---
layout: post
title: متباينة كوشي-شفارتس
tag: تحليل
---


# متباينة كوشي-شفارتس

متباينة كوشي-شفارتس هي من أهم المتباينات في الجبر الخطي والرياضيات التطبيقية، وتعطى كما يلي:

$$
\left( \sum_{i=1}^{n} a_i b_i \right)^2 \leq \left( \sum_{i=1}^{n} a_i^2 \right) \left( \sum_{i=1}^{n} b_i^2 \right)
$$

## البرهان

لنفرض لدينا متجهين \( \mathbf{a} = (a_1, a_2, \dots, a_n) \) و \( \mathbf{b} = (b_1, b_2, \dots, b_n) \) في الفضاء الإقليدي \( \mathbb{R}^n \).

نعتبر دالة المساعدة التالية:

$$
f(t) = \sum_{i=1}^{n} (a_i + t b_i)^2
$$

### الخطوة 1: تحليل الدالة

الدالة \( f(t) \) هي دالة تربيعية في \( t \). نوسع التعبير:

$$
f(t) = \sum_{i=1}^{n} (a_i^2 + 2 t a_i b_i + t^2 b_i^2)
$$

يمكن كتابة \( f(t) \) على شكل:

$$
f(t) = \sum_{i=1}^{n} a_i^2 + 2t \sum_{i=1}^{n} a_i b_i + t^2 \sum_{i=1}^{n} b_i^2
$$

وبالتالي:

$$
f(t) = A + 2Bt + Ct^2
$$

حيث:

- \( A = \sum_{i=1}^{n} a_i^2 \)
- \( B = \sum_{i=1}^{n} a_i b_i \)
- \( C = \sum_{i=1}^{n} b_i^2 \)

### الخطوة 2: شرط غير سلبية الدالة

بما أن \( f(t) \geq 0 \) لجميع قيم \( t \) لأن مربع أي عدد حقيقي هو دائمًا غير سالب، فإن المميز الخاص بالمعادلة التربيعية \( f(t) = 0 \) يجب أن يكون غير موجب. أي أن:

$$
\Delta = B^2 - AC \leq 0
$$

### الخطوة 3: النتيجة

من الشرط أعلاه، نحصل على:

$$
B^2 \leq AC
$$

أي:

$$
\left( \sum_{i=1}^{n} a_i b_i \right)^2 \leq \left( \sum_{i=1}^{n} a_i^2 \right) \left( \sum_{i=1}^{n} b_i^2 \right)
$$

وهذا ما يثبت متباينة كوشي-شفارتس.
