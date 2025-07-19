---
layout: post
title: "نموذج لانشستر للقتال (Lanchester Combat Model)"
description: "نموذج رياضي لوصف ديناميكيات الصراع بين قوتين متحاربتين باستخدام المعادلات التفاضلية"
tag: تحليل
author: Bachir
---
<br>
## مقدمة تاريخية
في عام 1916، وضع المهندس الإنجليزي فريدريك لانشستر (Frederick Lanchester) نموذجاً رياضياً ثورياً لوصف الصراعات بين جيشين متحاربين. جاء هذا العمل خلال الحرب العالمية الأولى، عندما كانت الأسلحة الحديثة وتقنيات القتال بعيدة المدى تغير طبيعة المعارك جذرياً.

قبل عصر الأسلحة النارية، كان كل جندي يقاتل جندياً واحداً من العدو في نفس الوقت، مما يعني أن النتيجة تعتمد ببساطة على الفرق في أحجام الجيشين. لكن ظهور الأسلحة بعيدة المدى غيّر هذه القواعد تماماً.

## نموذج لانشستر الأساسي
نموذج لانشستر يصف التغير في قوة الجيشين عبر الزمن باستخدام نظام من المعادلات التفاضلية:

$$
\begin{split}
\frac{dR(t)}{dt} &= -b B(t) \\
\frac{dB(t)}{dt} &= -r R(t)
\end{split}
$$

حيث:
- $R(t)$ عدد جنود الجيش الأحمر في الزمن $t$
- $B(t)$ عدد جنود الجيش الأزرق في الزمن $t$  
- $b$ معامل فعالية الجيش الأزرق (قدرة كل جندي أزرق على قتل الجنود الحمر)
- $r$ معامل فعالية الجيش الأحمر (قدرة كل جندي أحمر على قتل الجنود الزرق)

## قانون لانشستر التربيعي
من خلال حل هذا النظام من المعادلات التفاضلية، نحصل على **قانون لانشستر التربيعي**:

$$
r R^2(t) - b B^2(t) = r R_0^2 - b b_0^2 =\text{تباث}
$$

حيث $R_0$ و $B_0$ هما هي العدد الإبتدائي للجنود للجيشين (الأحمر، و الأزرق على التوالي).

**النتيجة المذهلة**: قوة الجيش تتناسب مع **مربع** عدد جنوده، وليس مع العدد نفسه!

## التطبيقات والنتائج
هذا النموذج يقدم رؤى مهمة:

1. **تفوق التركيز**: جيش واحد كبير أقوى من جيشين صغيرين بنفس العدد الإجمالي
2. **أهمية الجودة**: تحسين فعالية الأسلحة ($\alpha$ أو $\beta$) له تأثير مضاعف
3. **التنبؤ بالنتائج**: يمكن التنبؤ بنتيجة المعركة من الظروف الأولية

## شرح بالفيديو
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
  <iframe 
    src="https://www.youtube.com/embed/Bc0GJlbBl3o?si=B-V20lHIi12EB4mh" 
    title="YouTube video player"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" 
    allowfullscreen>
  </iframe>
</div>

---
## المراجع
1. [N.J. MacKay, "Lanchester combat models", arXiv:math/0606300v1 [math.HO] 13 Jun 2006](https://arxiv.org/pdf/math/0606300.pdf)


<div id="comments">
  <script src="https://utteranc.es/client.js"
          repo="bachirmath/bachirmath.github.io"
          issue-term="pathname"
          theme="github-dark-orange"
          crossorigin="anonymous"
          async>
  </script>
</div>
