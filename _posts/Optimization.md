---
layout: post
title: Optimization
tag: Books
---

$$
\begin{split}\begin{array}{l}
\begin{array}{lcrcrcl}
 \max \mspace{-6mu}&\mspace{-6mu}  \mspace{-6mu}&\mspace{-6mu} 10 x \mspace{-6mu}&\mspace{-6mu} + \mspace{-6mu}&\mspace{-6mu} 5 y \mspace{-6mu} \\
 \mspace{-6mu}&\mspace{-6mu}  \mspace{-6mu}&\mspace{-6mu} x \mspace{-6mu}&\mspace{-6mu} + \mspace{-6mu}&\mspace{-6mu} y \mspace{-6mu}&\mspace{-6mu} \leq \mspace{-6mu}&\mspace{-6mu} 1000 \\
 \mspace{-6mu}&\mspace{-6mu}  \mspace{-6mu}&\mspace{-6mu} 3 x \mspace{-6mu}&\mspace{-6mu} + \mspace{-6mu}&\mspace{-6mu} y \mspace{-6mu}&\mspace{-6mu} \leq \mspace{-6mu}&\mspace{-6mu} 1500 \\
\end{array} \\
x, y \geq 0
\end{array}\end{split}
$$


<div class="sage">
  <script type="text/x-sage">
A = ([1, 1], [3, 1])
b = (1000, 1500)
c = (10, 5)
# Create an interactive linear programming problem
P = InteractiveLPProblem(A, b, c, ["x", "y"], variable_type=">=")
# Plot the feasible region and objective function
P.plot().show()
  </script>
</div>


[![PDF Preview](https://media.springernature.com/w316/springer-static/cover-hires/book/978-3-319-56769-3?as=webp)](https://drive.google.com/file/d/1c1bRNGaSNwjtfQu3dHuDI6KP-CS2wxMx/view?usp=sharing)


[![PDF Preview](https://media.springernature.com/w316/springer-static/cover-hires/book/978-0-387-68407-9?as=webp)](https://drive.google.com/file/d/1a2tw2woRz0QnaJwfLxYkK64gyFCi9TGs/view?usp=sharing)

[![PDF Preview](https://media.springernature.com/w316/springer-static/cover-hires/book/978-0-387-21680-5?as=webp)](https://drive.google.com/file/d/1KqsjUCE9eTBl80_gWCwMIfec47CBncOJ/view?usp=sharing)

[![PDF Preview](https://media.springernature.com/w316/springer-static/cover-hires/book/978-3-030-11184-7?as=webp)](https://drive.google.com/file/d/1kmoyqtMtDnS2goH_TBU8d3yyi1wVMXB_/view?usp=sharing)


[![PDF Preview](https://media.springernature.com/w316/springer-static/cover-hires/book/978-3-030-72819-9?as=webp)](https://drive.google.com/file/d/1hWMm-INCU5Jn-K3m9FGRKxqBAXKhZQ42/view?usp=sharing)


<script src="https://utteranc.es/client.js"
        repo="bachirmath/bachirmath.github.io"
        issue-term="pathname"
        theme="github-dark-orange"
        crossorigin="anonymous"
        async>
</script>
