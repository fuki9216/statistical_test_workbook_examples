## 統計検定準1級(Statistical Test Pre-1st grade)
## 2章 例1
### 回答
周辺確率密度関数は

$-1\leq x \leq 1$ の場合の同時確率密度関数が正となる$y$の範囲は $-\sqrt{1-x^2}\leq y \leq \sqrt{1-x^2}$ となる

$x$ の周辺確率密度関数は

$$
\int^{\sqrt{1-x^2}}_{-\sqrt{1-x^2}} \frac{1}{\pi} dy
$$

で積分する

$$
\frac{1}{\pi} \int^{\sqrt{1-x^2}}_{-\sqrt{1-x^2}}dy
$$

1が無い場合はその範囲を返す

$$
\sqrt{1-x^2}- (-\sqrt{1-x^2}) = 2\sqrt{1-x^2}\\

$$

積分結果(周辺確率密度関数)は

$$
\frac{2\sqrt{1-x^2}}{\pi}

$$

条件付き確率密度関数は

$$
f_{Y|X}(y|x) = \frac{f(x, y)}{f_x (x)}
$$

となり、一様分布なので

$$
f_{Y|X}(y|x)\\
 = \frac{1}{\pi}\cdot \frac{\pi}{2\sqrt{1-x^2}}
\\
= \frac{1}{2\sqrt{1-x^2}}
$$