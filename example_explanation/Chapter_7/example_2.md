## 統計検定準1級(Statistical Test Pre-1st grade)
## 7章 例2
### 回答

分布収束は以下で計算ができる

$$
lim_{n→\infty}F_n(x) = G(x)
$$

$Z = \frac{x- \mu}{\sigma}$より

$Z = \frac{x-0}{\sqrt{\frac{1}{n}}}= \sqrt{n}x$
 

このZ値と累積分布関数を利用して式変換する

累積分布関数

$$
\Phi(z)=\int^z_{-\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}dx\\
$$

この $\Phi(z)$ は0〜1の値を取り、

$\Phi(z) = \Phi(\sqrt{n}x)$ となる

$x\geq 0$ で$Z→\infty$ 
$x\leq0$ で$Z→0$ 

に収束する

よって

$x\geq 0$ で1 
$x\leq0$ で0

に収束する