تحويل لابلاس و تطبيقاته
=======================

مفاهيم و تعاريف
---------------

في ما يلي،كل الدوال معرفة من أجل $x\geq 0$ (أو $x>0$).

لتكن $f$ دالة، يسمى
$$\mathscr{L}(f)(s):=\int_{0}^{+\infty}f(x)e^{-sx}dx$$ (في حالة تقارب
التكامل)، **[بتحويل لابلاس]{.underline}** ل $f$.

1.  لنعتبر الدالة التالية المسماة بدالة هيفيسايد
    [**[Heaviside]{lang="en"}**]{.underline}
    $$\mathcal{U}(x):=\begin{cases}1, \quad x\geq0\\
        0, \quad x<0
        \end{cases}$$

     

     

     

    (13,5.5) (-150,0)

    لنحسب تحويل لابلاس الخاص بها $$\begin{split}
        \mathscr{L}(\mathcal{U})(p):&=\int_{0}^{+\infty}\mathcal{U}(x)e^{-px}dx\\
        &=\int_{0}^{+\infty}e^{-px}dx=\frac{-e^{-px}}{p}\bigg|_0^{+\infty}\\
        \mathscr{L}(\mathcal{U})(p)&=\frac{1}{p}, \quad \forall p>0.\\
       \end{split}$$

     

2.  لنعتبر الدالة $f_n(x)=x^n$، تحويل لابلاس الخاص بها هو
    $$\begin{split}
    \mathscr{L}(f_n)(p):&=\int_{0}^{+\infty}x^ne^{-px}dx\\
    &=\frac{-x^ne^{-px}}{p}\Bigg|_0^{+\infty}+\frac{n}{p}\int_{0}^{+\infty}x^{n-1}e^{-px}dx\\
    &=\frac{n}{p}\mathscr{L}(f_{n-1})(p)\\
    &=\Big(\frac{n}{p}\Big)\Big(\frac{n-1}{p}\Big)\cdots\Big(\frac{1}{p}\Big)\mathscr{L}(f_{0})(p)\\
    &=\frac{n!}{p^n}\mathscr{L}(\mathcal{U})(p)\\
    \mathscr{L}(f_n)(p)&=\frac{n!}{p^{n+1}},\quad \forall p>0.
    \end{split}$$

3.  كمثال لدالة لا تقبل تحويل لابلاس، نعتبر $$f(x)=e^{x^2}$$ تحويل
    لابلاس لهذه الدالة غير موجود، لأن $$\int_{0}^{+\infty}e^{x^2-px}dx$$
    غير محدود مهما كان $p>0$.

 

 

 

 

كما رأينا في المثال السابق، يمكن ل $f$ أن لا تقبل تحويل لابلاس. نسأل هنا
تحت أي شرط (على $f$) يمكن أن نضمن وجود تحويل لابلاس لها؟، للجواب عليه
نبدأ بالتعريف التالي

نقول عن $f:\R^+\rightarrow \R$ أنها مستمرة بالقطع، إذا كان من أجل كل
$[a,b]\subset\R^+$ (محدود)، يوجد $\{x_i\}_{i=1}^n$ حيث
$[a,b]=\bigcup\limits_{i=1}^{n-1}[x_i,x_{i+1}]$، $f$ مستمرة على كل مجال
$]x_i,x_{i+1}[$ و
$$\lim_{x\underset{>}{\to} x_i} |f(x)|<\infty, \quad \lim_{x\underset{<}{\to} x_i} |f(x)|<\infty, \quad \forall i$$

 

(9,6.5) (-1,0)

[\[vboprt\]]{#vboprt label="vboprt"} لنفرض أن $f:\R^+\rightarrow \R$
تحقق

1.  $f$ مستمرة بالقطع،

2.  يوجد $a, M, \bar{x}>0$ حيث
    $$\forall x>\bar{x}, \quad |f(x)|\leq Me^{ax}$$

فإن تحويل لابلاس ل $f$ موجود من أجل $p>a$.

يكمن البرهان في إثبات أن التكامل متقارب، لنثبت ذلك نلاحظ أن $f$ محدودة
على كل مجال من الشكل $[0,A]$، و هذا يعني أن $f(x)e^{-px}$ تقبل المكاملة
على $[0,A]$، و بما أن

$$\int_{0}^{+\infty}f(x)e^{-px}dx=\int_{0}^{A}f(x)e^{-px}dx+\int_{A}^{+\infty}f(x)e^{-px}dx$$

و بأخذ $x_0<A$، نجد

$$\begin{aligned}
    \bigg|\int_{A}^{+\infty}f(x)e^{-px}dx\bigg|&\leq  \int_{A}^{+\infty}\Big|f(x)e^{-px}\Big|dx\\
    &\leq\int_{A}^{+\infty}M e^{ax}e^{-px}dx\\
    &\leq\frac{Me^{(a-p)x}}{a-p}\bigg|_{A}^{+\infty}\\
    &\leq\frac{Me^{(a-p)A}}{p-a}, \quad \forall p>a\end{aligned}$$

و هذا يعني أن التكامل يتقارب من أجل $a<p$.

-   يمكن أن نلاحظ في البرهان الأخير أنه تحت هذه الشروط، لدينا
    $\lim\limits_{p\to+\infty} \mathscr{L}(f)(p)=0$

-   الشرطين في النظرية السابقة كافيين، و ليسا لازمين عموما،
    $f(x)=\dfrac{1}{\sqrt{x}}$ كمثال.

لنعتبر الدالة $f(x)=e^{\alpha x}$، تحويل لابلاس الخاص بها هو
$$\begin{split}
  \mathscr{L}(e^{\alpha x})(p):&=\int_{0}^{+\infty}e^{\alpha x}e^{-px}dx\\
    &=\frac{e^{-(\alpha-p)x}}{\alpha-p}\bigg|_0^{+\infty}\\
    &=\frac{1}{p-\alpha}, \quad p>\alpha.
    \end{split}$$

 

خواص تحويل لابلاس 
-----------------

لتكن $f$ و $g$ دالتين كيفيتين تقبلان تحويل لابلاس ($\mathscr{L}(f)$ ،
$\mathscr{L}(g)$ على التوالي)، نلخص بعض الخواص لتحويل لابلاس في النظرية
التالية:

 

-   [$\mathscr{L}(\cdot)$ خطي]{.underline} ، و هذا يعني
    $$\forall \alpha,\beta\in\R, \quad  \mathscr{L}(\alpha f+\beta g)=\alpha\mathscr{L}(f)+\beta\mathscr{L}(g).$$

-   [تحويل $h(x)= f(ax)$]{.underline} (حيث $a>0$)
    $$\mathscr{L}(h)(p) =\frac{1}{a}\mathscr{L}\big(f\big)\Big(\frac{p}{a}\Big).$$

-   [تحويل $k(x)=\mathcal{U}(x-a)f(x-a)$]{.underline} (حيث $a>0$)
    $$\mathscr{L}(k)(p)=e^{-ap}\mathscr{L}(f)(p).$$

```{=html}
<!-- -->
```
-   واضح كون التكامل خطي.

-   نقوم بالتحويل $$dx=\frac{dt}{a}\Leftarrow   t=ax$$ فنجد
    $$\begin{aligned}
        \mathscr{L}(h)(p):&=\int_{0}^{+\infty}f(ax)e^{-px}dx\\
        &=\int_{0}^{+\infty}f(t)e^{-\big(\frac{p}{a}\big)t}\frac{dt}{a}\\
         &=\frac{1}{a}\int_{0}^{+\infty}f(t)e^{-\big(\frac{p}{a}\big)t}dt\\
         &=\frac{1}{a}\mathscr{L}\big(f\big)\Big(\frac{p}{a}\Big).
     \end{aligned}$$

-   $$\begin{aligned}
      \mathscr{L}(k)(p):&=\int_{a}^{+\infty}f(x-a)e^{-px}dx\\
      &=e^{-pa}\int_{a}^{+\infty}f(x-a)e^{-p(x-a)}dx\\
      &=e^{-pa}\int_{0}^{+\infty}f(t)e^{-pt}dt\\
      \mathscr{L}(k)(p)&=e^{-pa}\mathscr{L}(f)(p).
     \end{aligned}$$
