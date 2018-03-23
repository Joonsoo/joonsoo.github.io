# 전준수 | Joonsoo Jeon
- Software engineer

### Education

* Feb 2007-Feb 2010, B.S. in Computer Science, KAIST
* Feb 2010-Feb 2012, M.S. in Computer Science, KAIST (<a class="btn btn-default btn-sm narrow" href="http://giyeok.com/assets/thesis.pdf"><i class="fa fa-2 fa-file-o"></i> Thesis</a>)

### Work Experience

* Feb 2012-Feb 2014, Software Engineer, [S-Core](http://www.s-core.co.kr)
* Feb 2014-Feb 2016, Software Engineer, [Kakao](http://www.kakaocorp.com)
* Oct 2016-Jul 2017, Software Engineer, [Thenully](https://reworkapp.com)
* Aug 2017-Mar 2018, Software Engineer, [HonestFund](https://www.honestfund.kr)

### Projects

* Work Experience
  * 2010-2012, Trudio
    * Trudio is a reverse engineering assistant tool for heavily obfuscated binary executables. It includes instruction level execution trace extractor developed using [Pintool](https://software.intel.com/en-us/articles/pin-a-dynamic-binary-instrumentation-tool) and trace analyzer implemented in [Java](). Prototype of the trace analyzer was implemented using [Python]() and [wxPython]().
    * You can download the trace extractor and trace analyzer [here](https://code.google.com/archive/p/trudio/downloads). Paper is [here](http://giyeok.com/assets/thesis.pdf)(korean) and [here](http://giyeok.com/assets/trudio.pdf)(english draft). Source code is not open.
  * 2012-2013, Tizen SDK and webida, S-Core
  * 2014-2015, KakaoTalk server, Kakao
  * 2016-2017, Rework app server, Thenully

* Personal Projects
  * 2013-2017, J Parser, A scannerless parser implementation <a class="btn btn-default narrow" href="https://github.com/joonsoo/jparser"><i class="fa fa-2 fa-github"></i>GitHub</a>
    * I proposed Conditional Derivation Grammar(CDG), that extends Context-Free Grammar with _conditional nonterminals_: longest match, intersection, exclusion, followed-by, and not-followed-by. It is designed to be capable of integrating lexical grammar with CFG and modeling modern programming languages.
    * I also devised a parsing algorithm for CDG. The algorithm is similar to [Earley parsing](https://en.wikipedia.org/wiki/Earley_parser), but it uses graph to represent the state of parsing and introduces _accept condition_ for conditional nonterminals.
    * The time and space complexity of the proposed algorithm differs according to the given grammars. If the given grammar does not have any conditional nonterminals, its time complexity will be same with Earley parsing, that is, O(n) for LR(k) grammars, O(n^2) for unambiguous grammars, and O(n^3) in general cases. Speaking of the grammars with conditional nonterminals, it may run in exponential time complexity to the length of the input string. However, it is only the hypothetical upper bound of the time complexity, and it is yet unknown if such grammar exists. I expect the algorithm to run in practical time complexity in real usages.
    * J Parser is an implementation of the proposed algorithm written in Scala. It also provides visualization using [SWT](https://www.eclipse.org/swt/), Eclipse [draw2d](https://www.eclipse.org/gef/draw2d/) and [zest](https://www.eclipse.org/gef/zest/).

  * 2017, Passzero, Secure password manager <a class="btn btn-default narrow" href="https://github.com/joonsoo/passzero"><i class="fa fa-2 fa-github"></i>GitHub</a>
    * A clone of 1password for personal use. It stores a randomly created secret key encrypted by user defined password in local storage, and encrypts private password information by the local secret key and saves to DropBox.
    * It is written in Scala. The GUI was implemented using [SWT](https://www.eclipse.org/swt/), but I am working on a new version of GUI using [JavaFX](http://www.oracle.com/technetwork/java/javase/overview/javafx-overview-2158620.html) for a better compatibility.

  * 2013, Dexdio, Dalvik executable reverse engineering tool <a class="btn btn-default narrow" href="https://github.com/joonsoo/dexdio"><i class="fa fa-2 fa-github"></i>GitHub</a>

  * 2013, Tournament manager, Web-based tournament game manager
    * A private web application project to manage tournament matches. It successfully held several tournament matches with dozens of players.

  * 2013, Gitexplorer, Git repository visualization tool <a class="btn btn-default narrow" href="https://github.com/joonsoo/gitexplorer"><i class="fa fa-2 fa-github"></i>GitHub</a>

  * 2009, Giyeok programming language, A scripting language <a class="btn btn-default narrow" href="https://github.com/joonsoo/giyeok"><i class="fa fa-2 fa-github"></i>GitHub</a>
    * A programming language made just for fun while taking a programming language course. It is written in C++, but it crashes if an incorrect program is given and does not properly manage the memory resources(a lot of memory leaks!) <i class="fa fa-smile-o"></i>.


### For Fun
  * <a href="https://cdn.rawgit.com/Joonsoo/identicon/150e1e39/index.html">(GitHub-like) Identicon Generator</a>

### Interests

* Program analysis
  * Software development tools
  * Automated test case generation
* Blockchain
* Machine learning
* 3D scanners and printers
* Automated farming

### Contacts
<i class="fa fa-2 fa-envelope-o"></i> <a href="mailto:giyeok7@gmail.com">giyeok7@gmail.com</a>  
<i class="fa fa-2 fa-mobile"></i> +82 10-6660-6540
<a class="btn btn-default narrow" href="https://github.com/joonsoo"><i class="fa fa-3 fa-github"></i></a>
<a class="btn btn-default narrow" href="https://www.facebook.com/joonsoo.jeon"><i class="fa fa-3 fa-facebook"></i></a>
<a class="btn btn-default narrow" href="https://www.linkedin.com/in/joonsoojeon"><i class="fa fa-3 fa-linkedin"></i></a>
