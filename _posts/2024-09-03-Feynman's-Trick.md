---
layout: post
title: طريقة فاينمان للمكاملة
tag: تحليل
---

طريقة فاينمان في التكامل هي إحدى طرق المكاملة التي تعتمد على نظرية لايبنيتز للإشتقاق تحت رمز المكاملة و هي إحدى النظريات الهامة في التحليل الدالي

## نظرية لايبنيتز

نظرية لايبنيتز للإشتقاق تحت رمز المكاملة تقول أنه إذا كانت هناك دالة \\(f(x,t)\\) من الصنف $$\mathcal{C}^1$$ ،أي أن $$f_t,f_x,f$$ مستمرة، <strong>  فإن</strong>

\begin{equation}
\frac{d}{dt} \int_a^b f(x, t)dx = \int_a^b \frac{\partial f(x, t)}{\partial t}dx
\end{equation}



### مثال 1:

لنعتبر التكامل التالي 
\begin{equation}
 \int_{0}^{1} \frac{\ln(x+1)}{x^2+1}dx
\end{equation}

<br>


## شرح بالفيديو

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
  <iframe 
    src="https://www.youtube.com/embed/IKGiPwgSFrk?si=q-714VkDAWVHEcIj" 
    title="YouTube video player"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" 
    allowfullscreen>
  </iframe>
</div>

<br>


<br>


### مثال 2:

لنعتبر مثلا تكامل غوس، و هو أحد أهم التكاملات و الذي له تطبيقات في شتى فروع الرياضيات

\begin{equation}
 \int_{0}^{+\infty} e^{-x^2}dx
\end{equation}

<br>

## شرح بالفيديو


<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
  <iframe 
    src="https://www.youtube.com/embed/AflQCAFtgnA?si=qY05VwxaO4-U-SSV" 
    title="YouTube video player"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" 
    allowfullscreen>
  </iframe>
</div>


<br>

<br>


<script src="https://utteranc.es/client.js"
        repo="bachirmath/bachirmath.github.io"
        issue-term="pathname"
        theme="github-dark-orange"
        crossorigin="anonymous"
        async>
</script>

