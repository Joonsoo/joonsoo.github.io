---
layout: post
title:  "Basic Structure of Git Repository"
date:   2013-10-08 20:27:30 KST
categories: gitexplorer
---

A git repository is a directed acyclic graph(DAG) of git objects.
There are four types of git objects: blob, tree, commit, and tag.

[GitAbstractObject trait and GitObject class][GitAbstractObject]:
{% highlight scala %}
trait GitAbstractObject {
    val id: GitId

    lazy val content: Array[Byte] = actualContent

    protected def actualContent: Array[Byte]

    // TODO make it abstract and implement it on inherited classes
    def verify: Boolean = true
}

sealed abstract class GitObject extends GitAbstractObject {
    val objectType: GitObject.Types
}
{% endhighlight %}

[GitBlob][GitBlob], [GitTree][GitTree], [GitCommit][GitCommit], [GitTag][GitTag] classes:
{% highlight scala %}
abstract class GitBlob extends GitObject {
    val objectType = GitObject.Types.BLOB
}

abstract class GitTree extends GitObject {
    val objectType = GitObject.Types.TREE

    val entries: List[GitTree.Entry]    // a blob object or another tree object
}

abstract class GitCommit extends GitObject {
    val objectType = GitObject.Types.COMMIT

    val tree: GitId
    val parents: List[GitId]        // a commit object
    val author: Option[GitUser]
    val committer: Option[GitUser]
    val message: Array[Byte]
}

abstract class GitTag extends GitObject {
    val objectType = GitObject.Types.TAG

    val objId: GitId                // a commit object
    val objType: String
    val tagName: String
    val tagger: Option[GitUser]
    val message: Array[Byte]
}
{% endhighlight %}

[GitAbstractObject]: https://github.com/Joonsoo/gitexplorer/blob/master/src/main/scala/com/giyeok/gitexplorer/model/GitObjects.scala#L19-L32
[GitBlob]: https://github.com/Joonsoo/gitexplorer/blob/master/src/main/scala/com/giyeok/gitexplorer/model/GitObjects.scala#L120-L122
[GitTree]: https://github.com/Joonsoo/gitexplorer/blob/master/src/main/scala/com/giyeok/gitexplorer/model/GitObjects.scala#L136-L140
[GitCommit]: https://github.com/Joonsoo/gitexplorer/blob/master/src/main/scala/com/giyeok/gitexplorer/model/GitObjects.scala#L176-L187
[GitTag]: https://github.com/Joonsoo/gitexplorer/blob/master/src/main/scala/com/giyeok/gitexplorer/model/GitObjects.scala#L241-L249
