## 統計検定準1級(Statistical Test Pre-1st grade)
## 8章 例2
### 回答

独立に同一の正規分布 $N(\mu, v)$ に従う場合の尤度関数は $N(\mu, v)$ のときの確率密度関数の積と等しい

$$
L(\mu, v| X_1, X_2...X_n) = \prod^n_{i=1} f(X_i|\mu, v)
$$

確率密度関数は
$f(x|\mu, v) = \frac{1}{\sqrt{2\pi v}} \ exp(- \frac{(x -\mu)^2}{2v})$ より

$$
L(\mu, v| X_1, X_2...X_n) = \prod^n_{i=1}\frac{1}{\sqrt{2\pi v}} \ exp(- \frac{(x -\mu)^2}{2v})
$$

計算を簡単にするために対数を取る

確率密度関数の対数は

$$
log\ f(x|\mu, v) = -\frac{1}{2} log(2\pi v) - \frac{(x -\mu)^2}{2v}
$$

総和を取ると対数尤度関数となる
$log\ L(\mu, v| X_1, X_2...X_n) = -\frac{n}{2} log(2\pi v) - \frac{1}{2v}\sum^n_{i=1} (X_i - \mu)^2$ 

上記を平均 $\mu$ 、分散 $v$ で微分する

- $\mu$ の微分
$\mu$ が付いている部分のみ微分=0とする
    
    $$
    \frac{\partial}{\partial \mu} \Big( \sum^n_{i=1}(X_i - \mu)^2 \Big)\\
    = \sum^n_{i=1} 2(X_i - \mu)\cdot (-1)\\
    =-2\sum^n_{i=1} (X_i - \mu) = 0\\
    \sum^n_{i=1} (X_i - \mu) = 0\\
    \sum^n_{i=1}X_i - \sum^n_{i=1}\mu = 0\\
    \sum^n_{i=1}X_i - n\mu = 0\\
    \mu = \frac{1}{n}\sum^n_{i=1}X_i
    $$
    
    ※合成関数の微分：https://www.try-it.jp/chapters-7403/sections-7421/lessons-7438/question-2/
    
    よって標本平均となる
    

$$
\frac{\partial}{\partial v} log L (\mu, v) = -\frac{n}{2}log\ (2\pi v) - \frac{1}{2v}\sum^n_{i=1}(X_i - \mu)^2\\
= -\frac{n}{2}\cdot \frac{1}{v} -\frac{1}{2} \cdot (-\frac{1}{v^2})\sum^n_{i=1}(X_i - \mu)^2\\
= -\frac{n}{2v} + \frac{1}{2v^2}\sum^n_{i=1}(X_i - \mu)^2= 0
$$

両辺に $2v^2$ を掛けて

$$
\frac{n}{2v}=\frac{1}{2v^2}\sum^n_{i=1}(X_i - \mu)^2\\
nv=\sum^n_{i=1}(X_i - \mu)^2\\
v = \frac{1}{n}\sum^n_{i=1}(X_i - \mu)^2
$$

よって標本分散が最尤推定値となる