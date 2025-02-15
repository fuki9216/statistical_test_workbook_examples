## 統計検定準1級(Statistical Test Pre-1st grade)
## 4章 例1
### 回答
変換 $g(x) = X^2$ に基づき、

 $Y = X^2$ と定義すると、元の確率変数 $X$ に対応する $Y$ の値は $X$ の絶対値に依存する

つまり、 $X = \pm \sqrt{Y}$ 

標準正規分の確率密度関数 $f(x)$ は

$$
f(x) = \frac{1}{\sqrt{2\pi}}exp{(-\frac{x^2}{2}})\\

$$

となる

ただし、 $X = \pm \sqrt{Y}$ より$X^2$ となる変数は両方の符号を反映させるため2倍する

$$
=2 \cdot {\frac{1}{\sqrt{2\pi}}exp{(-\frac{x^2}{2}})}
$$

$g'(x) = 2X$ として

$\frac{f(x)}{|g'(x)|}$ より、 $g'(x)$ を割る

$$
\frac{2}{\sqrt{2\pi}}exp{(-\frac{x^2}{2}})\cdot \frac{1}{2x}\\
= \frac{1}{x\sqrt{2\pi}}exp{(-\frac{x^2}{2}})

$$

こちらに $y=x^2$ を適応

$$
= \frac{1}{\sqrt{2\pi y}}exp{(-\frac{y}{2}})
$$