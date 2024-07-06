<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="" xml:lang="">
<head>
  <meta charset="utf-8" />
  <meta name="generator" content="pandoc" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes" />
  <title>example4</title>
  <style>
    code{white-space: pre-wrap;}
    span.smallcaps{font-variant: small-caps;}
    span.underline{text-decoration: underline;}
    div.column{display: inline-block; vertical-align: top; width: 50%;}
    div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
    ul.task-list{list-style: none;}
  </style>
</head>
<body>
<h1 id="تحويل-لابلاس-و-تطبيقاته">تحويل لابلاس و تطبيقاته</h1>
<h2 id="مفاهيم-و-تعاريف">مفاهيم و تعاريف</h2>
<p>في ما يلي،كل الدوال معرفة من أجل <span class="math inline"><em>x</em> ≥ 0</span> (أو <span class="math inline"><em>x</em> &gt; 0</span>).</p>
<p>لتكن <span class="math inline"><em>f</em></span> دالة، يسمى <br /><span class="math display">ℒ(<em>f</em>)(<em>s</em>) := ∫<sub>0</sub><sup> + ∞</sup><em>f</em>(<em>x</em>)<em>e</em><sup> − <em>s</em><em>x</em></sup><em>d</em><em>x</em></span><br /> (في حالة تقارب التكامل)، <span><strong><span class="underline">بتحويل لابلاس</span></strong></span> ل <span class="math inline"><em>f</em></span>.</p>
<ol>
<li><p>لنعتبر الدالة التالية المسماة بدالة هيفيسايد <span class="underline"><strong><span lang="en">Heaviside</span></strong></span> <br /><span class="math display">$$\mathcal{U}(x):=\begin{cases}1, \quad x\geq0\\
    0, \quad x&lt;0
    \end{cases}$$</span><br /></p>
<p> </p>
<p> </p>
<p> </p>
<p>(13,5.5) (-150,0)</p>
<p>لنحسب تحويل لابلاس الخاص بها <br /><span class="math display">$$\begin{split}
    \mathscr{L}(\mathcal{U})(p):&amp;=\int_{0}^{+\infty}\mathcal{U}(x)e^{-px}dx\\
    &amp;=\int_{0}^{+\infty}e^{-px}dx=\frac{-e^{-px}}{p}\bigg|_0^{+\infty}\\
    \mathscr{L}(\mathcal{U})(p)&amp;=\frac{1}{p}, \quad \forall p&gt;0.\\
   \end{split}$$</span><br /></p>
<p> </p></li>
<li><p>لنعتبر الدالة <span class="math inline"><em>f</em><sub><em>n</em></sub>(<em>x</em>) = <em>x</em><sup><em>n</em></sup></span>، تحويل لابلاس الخاص بها هو <br /><span class="math display">$$\begin{split}
\mathscr{L}(f_n)(p):&amp;=\int_{0}^{+\infty}x^ne^{-px}dx\\
&amp;=\frac{-x^ne^{-px}}{p}\Bigg|_0^{+\infty}+\frac{n}{p}\int_{0}^{+\infty}x^{n-1}e^{-px}dx\\
&amp;=\frac{n}{p}\mathscr{L}(f_{n-1})(p)\\
&amp;=\Big(\frac{n}{p}\Big)\Big(\frac{n-1}{p}\Big)\cdots\Big(\frac{1}{p}\Big)\mathscr{L}(f_{0})(p)\\
&amp;=\frac{n!}{p^n}\mathscr{L}(\mathcal{U})(p)\\
\mathscr{L}(f_n)(p)&amp;=\frac{n!}{p^{n+1}},\quad \forall p&gt;0.
\end{split}$$</span><br /></p></li>
<li><p>كمثال لدالة لا تقبل تحويل لابلاس، نعتبر <br /><span class="math display"><em>f</em>(<em>x</em>) = <em>e</em><sup><em>x</em><sup>2</sup></sup></span><br /> تحويل لابلاس لهذه الدالة غير موجود، لأن <br /><span class="math display">∫<sub>0</sub><sup> + ∞</sup><em>e</em><sup><em>x</em><sup>2</sup> − <em>p</em><em>x</em></sup><em>d</em><em>x</em></span><br /> غير محدود مهما كان <span class="math inline"><em>p</em> &gt; 0</span>.</p></li>
</ol>
<p> </p>
<p> </p>
<p> </p>
<p> </p>
<p>كما رأينا في المثال السابق، يمكن ل <span class="math inline"><em>f</em></span> أن لا تقبل تحويل لابلاس. نسأل هنا تحت أي شرط (على <span class="math inline"><em>f</em></span>) يمكن أن نضمن وجود تحويل لابلاس لها؟، للجواب عليه نبدأ بالتعريف التالي</p>
<p>نقول عن <span class="math inline">$f:\R^+\rightarrow \R$</span> أنها مستمرة بالقطع، إذا كان من أجل كل <span class="math inline">$[a,b]\subset\R^+$</span> (محدود)، يوجد <span class="math inline">{<em>x</em><sub><em>i</em></sub>}<sub><em>i</em> = 1</sub><sup><em>n</em></sup></span> حيث <span class="math inline">$[a,b]=\bigcup\limits_{i=1}^{n-1}[x_i,x_{i+1}]$</span>، <span class="math inline"><em>f</em></span> مستمرة على كل مجال <span class="math inline">]<em>x</em><sub><em>i</em></sub>, <em>x</em><sub><em>i</em> + 1</sub>[</span> و <br /><span class="math display">$$\lim_{x\underset{&gt;}{\to} x_i} |f(x)|&lt;\infty, \quad \lim_{x\underset{&lt;}{\to} x_i} |f(x)|&lt;\infty, \quad \forall i$$</span><br /></p>
<p> </p>
<p>(9,6.5) (-1,0)</p>
<p><span id="vboprt" label="vboprt">[vboprt]</span> لنفرض أن <span class="math inline">$f:\R^+\rightarrow \R$</span> تحقق</p>
<ol>
<li><p><span class="math inline"><em>f</em></span> مستمرة بالقطع،</p></li>
<li><p>يوجد <span class="math inline"><em>a</em>, <em>M</em>, <em>x̄</em> &gt; 0</span> حيث <br /><span class="math display">∀<em>x</em> &gt; <em>x̄</em>,  |<em>f</em>(<em>x</em>)| ≤ <em>M</em><em>e</em><sup><em>a</em><em>x</em></sup></span><br /></p></li>
</ol>
<p>فإن تحويل لابلاس ل <span class="math inline"><em>f</em></span> موجود من أجل <span class="math inline"><em>p</em> &gt; <em>a</em></span>.</p>
<p>يكمن البرهان في إثبات أن التكامل متقارب، لنثبت ذلك نلاحظ أن <span class="math inline"><em>f</em></span> محدودة على كل مجال من الشكل <span class="math inline">[0, <em>A</em>]</span>، و هذا يعني أن <span class="math inline"><em>f</em>(<em>x</em>)<em>e</em><sup> − <em>p</em><em>x</em></sup></span> تقبل المكاملة على <span class="math inline">[0, <em>A</em>]</span>، و بما أن</p>
<p><br /><span class="math display">∫<sub>0</sub><sup> + ∞</sup><em>f</em>(<em>x</em>)<em>e</em><sup> − <em>p</em><em>x</em></sup><em>d</em><em>x</em> = ∫<sub>0</sub><sup><em>A</em></sup><em>f</em>(<em>x</em>)<em>e</em><sup> − <em>p</em><em>x</em></sup><em>d</em><em>x</em> + ∫<sub><em>A</em></sub><sup> + ∞</sup><em>f</em>(<em>x</em>)<em>e</em><sup> − <em>p</em><em>x</em></sup><em>d</em><em>x</em></span><br /></p>
<p>و بأخذ <span class="math inline"><em>x</em><sub>0</sub> &lt; <em>A</em></span>، نجد</p>
<p><br /><span class="math display">$$\begin{aligned}
    \bigg|\int_{A}^{+\infty}f(x)e^{-px}dx\bigg|&amp;\leq  \int_{A}^{+\infty}\Big|f(x)e^{-px}\Big|dx\\
    &amp;\leq\int_{A}^{+\infty}M e^{ax}e^{-px}dx\\
    &amp;\leq\frac{Me^{(a-p)x}}{a-p}\bigg|_{A}^{+\infty}\\
    &amp;\leq\frac{Me^{(a-p)A}}{p-a}, \quad \forall p&gt;a\end{aligned}$$</span><br /></p>
<p>و هذا يعني أن التكامل يتقارب من أجل <span class="math inline"><em>a</em> &lt; <em>p</em></span>.</p>
<ul>
<li><p>يمكن أن نلاحظ في البرهان الأخير أنه تحت هذه الشروط، لدينا <span class="math inline">$\lim\limits_{p\to+\infty} \mathscr{L}(f)(p)=0$</span></p></li>
<li><p>الشرطين في النظرية السابقة كافيين، و ليسا لازمين عموما، <span class="math inline">$f(x)=\dfrac{1}{\sqrt{x}}$</span> كمثال.</p></li>
</ul>
<p>لنعتبر الدالة <span class="math inline"><em>f</em>(<em>x</em>) = <em>e</em><sup><em>α</em><em>x</em></sup></span>، تحويل لابلاس الخاص بها هو <br /><span class="math display">$$\begin{split}
  \mathscr{L}(e^{\alpha x})(p):&amp;=\int_{0}^{+\infty}e^{\alpha x}e^{-px}dx\\
    &amp;=\frac{e^{-(\alpha-p)x}}{\alpha-p}\bigg|_0^{+\infty}\\
    &amp;=\frac{1}{p-\alpha}, \quad p&gt;\alpha.
    \end{split}$$</span><br /></p>
<p> </p>
<h2 id="خواص-تحويل-لابلاس">خواص تحويل لابلاس </h2>
<p>لتكن <span class="math inline"><em>f</em></span> و <span class="math inline"><em>g</em></span> دالتين كيفيتين تقبلان تحويل لابلاس (<span class="math inline">ℒ(<em>f</em>)</span> ، <span class="math inline">ℒ(<em>g</em>)</span> على التوالي)، نلخص بعض الخواص لتحويل لابلاس في النظرية التالية:</p>
<p> </p>
<ul>
<li><p><span class="underline"><span class="math inline">ℒ( ⋅ )</span> خطي</span> ، و هذا يعني <br /><span class="math display">$$\forall \alpha,\beta\in\R, \quad  \mathscr{L}(\alpha f+\beta g)=\alpha\mathscr{L}(f)+\beta\mathscr{L}(g).$$</span><br /></p></li>
<li><p><span class="underline">تحويل <span class="math inline"><em>h</em>(<em>x</em>) = <em>f</em>(<em>a</em><em>x</em>)</span></span> (حيث <span class="math inline"><em>a</em> &gt; 0</span>) <br /><span class="math display">$$\mathscr{L}(h)(p) =\frac{1}{a}\mathscr{L}\big(f\big)\Big(\frac{p}{a}\Big).$$</span><br /></p></li>
<li><p><span class="underline">تحويل <span class="math inline"><em>k</em>(<em>x</em>) = 𝒰(<em>x</em> − <em>a</em>)<em>f</em>(<em>x</em> − <em>a</em>)</span></span> (حيث <span class="math inline"><em>a</em> &gt; 0</span>) <br /><span class="math display">ℒ(<em>k</em>)(<em>p</em>) = <em>e</em><sup> − <em>a</em><em>p</em></sup>ℒ(<em>f</em>)(<em>p</em>).</span><br /></p></li>
</ul>
<ul>
<li><p>واضح كون التكامل خطي.</p></li>
<li><p>نقوم بالتحويل <br /><span class="math display">$$dx=\frac{dt}{a}\Leftarrow   t=ax$$</span><br /> فنجد <br /><span class="math display">$$\begin{aligned}
    \mathscr{L}(h)(p):&amp;=\int_{0}^{+\infty}f(ax)e^{-px}dx\\
    &amp;=\int_{0}^{+\infty}f(t)e^{-\big(\frac{p}{a}\big)t}\frac{dt}{a}\\
     &amp;=\frac{1}{a}\int_{0}^{+\infty}f(t)e^{-\big(\frac{p}{a}\big)t}dt\\
     &amp;=\frac{1}{a}\mathscr{L}\big(f\big)\Big(\frac{p}{a}\Big).
 \end{aligned}$$</span><br /></p></li>
<li><p><br /><span class="math display">$$\begin{aligned}
  \mathscr{L}(k)(p):&amp;=\int_{a}^{+\infty}f(x-a)e^{-px}dx\\
  &amp;=e^{-pa}\int_{a}^{+\infty}f(x-a)e^{-p(x-a)}dx\\
  &amp;=e^{-pa}\int_{0}^{+\infty}f(t)e^{-pt}dt\\
  \mathscr{L}(k)(p)&amp;=e^{-pa}\mathscr{L}(f)(p).
 \end{aligned}$$</span><br /></p></li>
</ul>
</body>
</html>
