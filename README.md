<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>JAG Sage and Python</title>
<meta name="Keywords" content="Authored in MathBook XML">
<meta name="viewport" content="width=device-width,  initial-scale=1.0, user-scalable=0, minimum-scale=1.0, maximum-scale=1.0">
<script type="text/javascript" src="https://sagecell.sagemath.org/static/jquery.min.js"></script><script type="text/x-mathjax-config">
// contrib directory for accessibility menu, moot after v2.6+?
MathJax.Ajax.config.path["Contrib"] = "https://cdn.mathjax.org/mathjax/contrib";
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['\\(','\\)']],
    },
    TeX: {
        // [Contrib]accessibility menu moot after v2.6+?
        extensions: ["AMSmath.js", "AMSsymbols.js", "extpfeil.js", "autobold.js", "https://aimath.org/mathbook/mathjaxknowl.js", "[Contrib]/a11y/accessibility-menu.js", ],
        equationNumbers: { autoNumber: "none",
                           useLabelIds: true,
                           // JS comment, XML CDATA protect XHTML quality of file
                           // if removed in XSL, use entities
                           //<![CDATA[
                           formatID: function (n) {return String(n).replace(/[:'"<>&]/g,"")},
                           //]]>
                         },
        TagSide: "right",
        TagIndent: ".8em",
    },
    "HTML-CSS": {
        scale: 88,
    },
});
    </script><script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML-full"></script><script type="text/javascript" src="https://sagecell.sagemath.org/embedded_sagecell.js"></script><script>$(function () {
    // Make *any* div with class 'sagecell-sage' an executable Sage cell
    // Their results will be linked, only within language type
    sagecell.makeSagecell({inputLocation: 'div.sagecell-sage',
                           linked: true,
                           languages: ['sage'],
                           evalButtonText: 'Evaluate Sage Code'});
});
</script><link href="https://aimath.org/knowlstyle.css" rel="stylesheet" type="text/css">
<script type="text/javascript" src="https://aimath.org/knowl.js"></script><script src="https://aimath.org/mathbook/js/lib/jquery.sticky.js"></script><script src="https://aimath.org/mathbook/js/lib/jquery.espy.min.js"></script><script src="https://aimath.org/mathbook/js/Mathbook.js"></script><link href="https://fonts.googleapis.com/css?family=Open+Sans:400,400italic,600,600italic" rel="stylesheet" type="text/css">
<link href="https://fonts.googleapis.com/css?family=Inconsolata:400,700&amp;subset=latin,latin-ext" rel="stylesheet" type="text/css">
<link href="https://aimath.org/mathbook/stylesheets/mathbook-3.css" rel="stylesheet" type="text/css">
<link href="https://aimath.org/mathbook/mathbook-add-on.css" rel="stylesheet" type="text/css">
<link href="jagbook.css" rel="stylesheet" type="text/css">
</head>
<body class="mathbook-book has-toc has-sidebar-left">
<a class="assistive" href="#content">Skip to main content</a><div style="display:none;">\(\newcommand{\Z}{\mathbb{Z}}
\newcommand{\reals}{\mathbb{R}}
\newcommand{\real}[1]{\mathbb{R}^{#1}}
\newcommand{\fe}[2]{#1\mathopen{}\left(#2\right)\mathclose{}}
\newcommand{\cinterval}[2]{\left[#1,#2\right]}
\newcommand{\ointerval}[2]{\left(#1,#2\right)}
\newcommand{\cointerval}[2]{\left[\left.#1,#2\right)\right.}
\newcommand{\ocinterval}[2]{\left(\left.#1,#2\right]\right.}
\newcommand{\point}[2]{\left(#1,#2\right)}
\newcommand{\fd}[1]{#1'}
\newcommand{\sd}[1]{#1''}
\newcommand{\td}[1]{#1'''}
\newcommand{\lz}[2]{\frac{d#1}{d#2}}
\newcommand{\lzn}[3]{\frac{d^{#1}#2}{d#3^{#1}}}
\newcommand{\lzo}[1]{\frac{d}{d#1}}
\newcommand{\lzoo}[2]{{\frac{d}{d#1}}{\left(#2\right)}}
\newcommand{\lzon}[2]{\frac{d^{#1}}{d#2^{#1}}}
\newcommand{\lzoa}[3]{\left.{\frac{d#1}{d#2}}\right|_{#3}}
\newcommand{\abs}[1]{\left|#1\right|}
\newcommand{\sech}{\operatorname{sech}}
\newcommand{\csch}{\operatorname{csch}}
\newcommand \dd[1]  { \,\textrm d{#1}                       }   
\newcommand \de[2]  { \frac{\mathrm d{#1}}{\mathrm d{#2}}   }   
\newcommand \intl[4]{ \int\limits_{#1}^{#2}{#3}\dd{#4}      }   

\newcommand\at[2]{\left.#1\right|_{#2}}
\newcommand{\lt}{ &lt; }
\newcommand{\gt}{ &gt; }
\newcommand{\amp}{ &amp; }
\)</div>
<header id="masthead" class="smallbuttons"><div class="banner"><div class="container">
<a id="logo-link" href="https://github.com/giannelli" target="_blank"><img src="images/jg.jpeg"></a><div class="title-container">
<h1 class="heading"><a href="index.html"><span class="title">John Giannelli</span><span class="subtitle">Musings on Sage Math</span></a></h1>
<p class="byline"></p>
</div>
</div></div>
<nav id="primary-navbar"><div class="container">
<div class="navbar-top-buttons">
<button class="sidebar-left-toggle-button button active" onclick="window.location.href='index.html'">Contents</button><div class="tree-nav toolbar toolbar-divisor-3">
<a class="index-button toolbar-item button" href="index-part-1.html" title="Index" alt="Index">Index</a><span class="threebuttons"><a class="previous-button toolbar-item button" href="section-6.html" title="Previous" alt="Previous">Prev</a><a class="up-button button toolbar-item" href="basics.html" title="Up" alt="Up">Up</a><a class="next-button button toolbar-item" href="integers.html" title="Next" alt="Next">Next</a></span>
</div>
<button class="sidebar-right-toggle-button button active">Annotations</button>
</div>
<div class="navbar-bottom-buttons toolbar toolbar-divisor-4">
<button class="sidebar-left-toggle-button button toolbar-item active">Contents</button><a class="previous-button toolbar-item button" href="section-6.html" title="Previous" alt="Previous">Prev</a><a class="up-button button toolbar-item" href="basics.html" title="Up" alt="Up">Up</a><a class="next-button button toolbar-item" href="integers.html" title="Next" alt="Next">Next</a>
</div>
</div></nav></header><div class="page">
<aside id="sidebar-left" class="sidebar"><div class="sidebar-content">
<nav id="toc"><h2 class="link"><a href="frontmatter.html"><span class="title">Front Matter</span></a></h2>
<ul>
<li><a href="biography-1.html">About John A Giannelli</a></li>
<li><a href="dedication-1.html">Dedication</a></li>
<li><a href="acknowledgement-1.html">Acknowledgements</a></li>
<li><a href="preface-1.html">Preface</a></li>
</ul>
<h2 class="link"><a href="sets.html"><span class="codenumber">1</span><span class="title">Quick Guide to Using SageMath</span></a></h2>
<ul>
<li><a href="sage-online.html">SageMath Online</a></li>
<li><a href="section-2.html">Running From Source</a></li>
</ul>
<h2 class="link active"><a href="basics.html"><span class="codenumber">2</span><span class="title">Basic Sage Commands</span></a></h2>
<ul>
<li><a href="section-3.html">Executing Sage Commands</a></li>
<li><a href="section-4.html">How to define functions</a></li>
<li><a href="section-5.html">Symbolic Manipulation</a></li>
<li><a href="section-6.html">Declaring Variables and Plotting</a></li>
<li><a href="section-7.html" class="active">Sage and Python</a></li>
</ul>
<h2 class="link"><a href="integers.html"><span class="codenumber">3</span><span class="title">Calculus</span></a></h2>
<ul>
<li><a href="calculus-limits.html">Calculating Limits</a></li>
<li><a href="section-product-rule.html">The Product Rule</a></li>
<li><a href="calculus-derivatives.html">Derivatives</a></li>
<li><a href="calculus-integration.html">Integration</a></li>
<li><a href="level-curves.html">Sketching Level Curves</a></li>
<li><a href="cap-2017-hw2.html">CAP 2017, HW 2 due January 31</a></li>
<li><a href="cap-2017-hw3.html">CAP 2017, HW 3 due February 7</a></li>
<li><a href="cap-2017-hw4.html">CAP 2017, HW 4 due February 14</a></li>
<li><a href="cap-2017-hw5.html">CAP 2017, HW 4 due February 28</a></li>
<li><a href="references-2.html">References</a></li>
</ul>
<h2 class="link"><a href="differential.html"><span class="codenumber">4</span><span class="title">Differential Equations</span></a></h2>
<ul>
<li><a href="first-order-de.html">First Order Differential Equations</a></li>
<li><a href="second-order-de.html">Second Order Differential Equations</a></li>
<li><a href="system-of-de.html">Systems Of Equations</a></li>
<li><a href="exercises-de.html">Exercises</a></li>
<li><a href="references-3.html">References (places I plagiarized)</a></li>
</ul>
<h2 class="link"><a href="linear-algebra-exam.html"><span class="codenumber">5</span><span class="title">Linear Algebra</span></a></h2>
<ul>
<li><a href="section-20.html">A1</a></li>
<li><a href="section-21.html">A2</a></li>
<li><a href="section-22.html">A3</a></li>
</ul>
<h2 class="link"><a href="backmatter.html"><span class="title">Back Matter</span></a></h2>
<ul>
<li><a href="appendix-1.html">Notation</a></li>
<li><a href="appendix-2.html">Hints and Solutions to Selected Exercises</a></li>
<li><a href="appendix-gfdl.html">GNU Free Documentation License</a></li>
<li><a href="index-part-1.html">Index</a></li>
<li><a href="colophon-1.html">Colophon</a></li>
</ul></nav><div class="extras"><nav><a class="mathbook-link" href="https://mathbook.pugetsound.edu">Authored in MathBook XML</a><a href="https://www.mathjax.org"><img title="Powered by MathJax" src="https://cdn.mathjax.org/mathjax/badge/badge.gif" border="0" alt="Powered by MathJax"></a></nav></div>
</div></aside><main class="main"><div id="content" class="mathbook-content"><section class="section" id="section-7"><header title="Section 2.5 Sage and Python"><h1 class="heading hide-type" alt="Section 2.5 Sage and Python">
<span class="type">Section</span><span class="codenumber">2.5</span><span class="title">Sage and Python</span>
</h1></header><p id="p-52">
            Sage is built on top of <a class="external-url" href="https://www.python.org/" target="_blank">Python</a>. It will do no harm to find
            out a little about this programming language and will aid your understanding of some of the
            examples used in this manual.
        </p>
<section class="subsection" id="subsection-5"><header title="Subsection 2.5.1 Lists, Tuples, and Dictionaries"><h1 class="heading hide-type" alt="Subsection 2.5.1 Lists, Tuples, and Dictionaries">
<span class="type">Subsection</span><span class="codenumber">2.5.1</span><span class="title">Lists, Tuples, and Dictionaries</span>
</h1></header><p id="p-53">Python has a number of built in data types. We will look at three that will come up again and again
            in this manual.</p>
<section class="subsubsection" id="subsubsection-1"><header title="Subsubsection 2.5.1.1 Lists"><h1 class="heading hide-type" alt="Subsubsection 2.5.1.1 Lists">
<span class="type">Subsubsection</span><span class="codenumber">2.5.1.1</span><span class="title">Lists</span>
</h1></header><p id="p-54">Creating Lists</p>
<ol id="ol-1" style="list-style-type: decimal;">
<li id="li-14">
<p id="p-55">To create a list of items then use the <tt class="code-inline tex2jax_ignore">[]</tt> operator filled with the items:</p>
<div class="sagecell-sage" id="sage-18"><script type="text/x-sage"># Creating lists with Python
listTransport = ['car', 'bus', 'train', 'plane', 'ship']
print("A list of vehicles: " + str(listTransport))

listNumbers = [5, 7, 9, 11, 13]
print("Some odd numbers: " + str(listNumbers))
</script></div>

</div>
</body>
</html>
