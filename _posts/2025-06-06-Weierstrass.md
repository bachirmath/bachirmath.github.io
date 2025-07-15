---
layout: post
title: "دالة  فايرشتراس (Weierstrass Function)"
description: "دالة مستمرة في كل نقطة لكنها غير قابلة للاشتقاق في أي نقطة"
tag: تحليل
author: Bachir
---
<br>

## مقدمة تاريخية

في عام 1872، قدم العالم الألماني كارل وايرستراس (Karl Weierstrass) مثالاً مذهلاً هز الأوساط الرياضية: دالة مستمرة في كل نقطة لكنها غير قابلة للاشتقاق في أي نقطة. قبل هذا الاكتشاف، كان الاعتقاد السائد أن الدوال المستمرة تكون قابلة للاشتقاق في معظم النقاط.

## دالة  فايرشتراس

دالة وايرستراس تُعرف بالسلسلة:

$$
W(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x)
$$

حيث $0 < a < 1$ و $b$ عدد صحيح موجب فردي.

**النتيجة الأساسية**: إذا كان $ab > 1 + \frac{3\pi}{2}$، فإن $W(x)$ مستمرة في كل نقطة وغير قابلة للاشتقاق في أي نقطة.

## نتيجة هاردي (Hardy's Result)

في عام 1916، أثبت جودفري هاردي (G.H. Hardy) نتيجة أقوى وأكثر دقة:

**نظرية هاردي**: إذا كان $ab \geq 1$، فإن دالة وايرستراس $W(x)$ غير قابلة للاشتقاق في أي نقطة.

هذه النتيجة حسّنت الشرط الأصلي لوايرستراس وقدمت برهاناً أكثر أناقة ودقة.

---

## المراجع

1. [Harry Dym, "Weierstrass's non-differentiable function", American Mathematical Society Transactions](https://www.ams.org/journals/tran/1916-017-03/S0002-9947-1916-1501044-1/S0002-9947-1916-1501044-1.pdf)
2. [Julian Havil, "Curves for the Mathematically Curious: An Anthology of the Unpredictable, Historical, Beautiful, and Romantic", Princeton University Press, 2019](https://press.princeton.edu/books/hardcover/9780691180052/curves-for-the-mathematically-curious)
