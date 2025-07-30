---
layout: post
title: "متتالية فيبوناتشي"
description: "استكشاف الخصائص الرياضية والتطبيقات الطبيعية لإحدى أشهر المتتاليات في الرياضيات"
tag: تحليل
author: Bachir
---

<br>

## مقدمة تاريخية
تُنسب متتالية فيبوناتشي إلى عالم الرياضيات الإيطالي ليوناردو فيبوناتشي (Leonardo Fibonacci) الذي عاش في القرن الثالث عشر. ظهرت هذه المتتالية لأول مرة في كتابه "Liber Abaci" عام 1202، من خلال مسألة شهيرة حول تكاثر الأرانب.

المسألة الأصلية: "إذا وُضع زوج من الأرانب في مكان مُحاط، فكم زوجاً من الأرانب سينتج عنهما في سنة واحدة، بافتراض أن كل زوج ينتج زوجاً جديداً كل شهر بدءاً من الشهر الثاني؟"

## تعريف المتتالية
متتالية فيبوناتشي تُعرّف رياضياً بالعلاقة التكرارية التالية:


$$
\begin{cases}
F_{n+2} = F_{n+1} + F_{n}, \quad  n \geq 1\\ \\
F_1 = 1, \quad F_2 = 1
\end{cases}
$$

هذا يعطينا المتتالية الشهيرة:

$$ 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...$$

## الخصائص الرياضية المذهلة

### النسبة الذهبية (Golden Ratio)

أحد أهم خصائص متتالية فيبوناتشي هو أن نسبة كل حد إلى الحد السابق تقترب من النسبة الذهبية:

$$\lim_{n \to \infty} \frac{F_{n+1}}{F_n} = \phi = \frac{1 + \sqrt{5}}{2} \approx 1.618$$

### صيغة بينيه (Binet's Formula)
يمكن حساب الحد النوني مباشرة دون الحاجة للحدود السابقة:

$$\boxed{F_n = \frac{\phi^{n} - (1-\phi)^{n}}{\sqrt{5}}}$$



### برنامج لحساب حدود المتتالية

<div class="sage">
  <script type="text/x-sage">
def F(n):
    phi = (1 + sqrt(5)) / 2
    Fn = (phi^(n) - (1 - phi)^(n)) / sqrt(5)
    return round(Fn)
# مثال: نحسب F(7)
print(F(7))  # الناتج يجب أن يكون 13
  </script>
</div>

## التطبيقات في الطبيعة
متتالية فيبوناتشي تظهر بشكل مدهش في الطبيعة:

- **النباتات**: عدد البتلات في الأزهار $(3, 5, 8, 13...)$
- **الأشجار**: ترتيب الأوراق والأغصان
- **الصنوبر**: ترتيب الحراشف في مخاريط الصنوبر
- **عباد الشمس**: ترتيب البذور في قرص الزهرة
- **الأصداف البحرية**: الشكل الحلزوني للقواقع

## التطبيقات العملية
- **الخوارزميات**: البحث الذهبي في التحسين
- **التمويل**: تحليل الأسواق المالية ونسب فيبوناتشي
- **الفن والعمارة**: استخدام النسبة الذهبية في التصميم
- **علوم الحاسوب**: هياكل البيانات والخوارزميات

## شرح بالفيديو
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
  <iframe 
    src="https://www.youtube.com/embed/2vWgb3IaEeI?si=28yY4a7EjeDwXVMy" 
    title="YouTube video player"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" 
    allowfullscreen>
  </iframe>
</div>

---
## المراجع
1. [Nicolai N. Vorobiev, Fibonacci Numbers, Birkhäuser Basel,2002. ](https://drive.google.com/file/d/1wYUvE3utteewb72lqvJacESGrFkRfcCO/view?usp=sharing)
2. [Dunlap, Richard A. "The Golden Ratio and Fibonacci Numbers", world Scientific, 1997](https://drive.google.com/file/d/19iLKD9QnVMBQrcxlc3ko-oeVoi5gJvrp/view?usp=sharing)

<div id="comments">
  <script src="https://utteranc.es/client.js"
          repo="bachirmath/bachirmath.github.io"
          issue-term="pathname"
          theme="github-dark-orange"
          crossorigin="anonymous"
          async>
  </script>
</div>
