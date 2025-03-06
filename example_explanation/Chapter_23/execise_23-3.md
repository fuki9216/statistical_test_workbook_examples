## 統計検定準1級(Statistical Test Pre-1st grade)
## 23章 例題3
### 回答

ベイスの定理を用いて分母と分子をそれぞれ表す

$P(y=1| X) = \frac{P(X|y=1)P(y=1)}{P(x|y=1)P(y=1) + P(X|y=-1)P(y= -1)}$

$P(y=-1|X) = \frac{P(X|y=-1)P(y=-1)}{P(x|y=1)P(y=1) + P(X|y=-1)P(y= -1)}$

上記より

$$
f(x) = log\ \frac{P(y=1|X)}{P(y=-1|X)}\\
= log\ \frac{P(X|y=1)P(y=1)}{P(X|y=-1)P(y=-1)}\\
$$

問題より

事前分布：$P(y=1), P(y=-1)$はそれぞれ$\pi_1, \pi_2$

$$
log\ \frac{P(X|y=1)\pi_1}{P(X|y=-1)\pi_2}\\
= log\ \frac{P(X|y=1)}{P(X|y=-1)} + log\ \frac{\pi_1}{\pi_2}\\

$$

問題より

$P(X|y=1), P(X|y=-1)$はそれぞれ$N(\mu_1, \Sigma_1), N(\mu_2, \Sigma_2)$に従うので、確率は

$$
P(X|y=1) = \frac{1}{\sqrt{2\pi \Sigma_1}} e^{-\frac{(x-\mu_1)^2}{2\Sigma_1}}\\
P(X|y=-1) = \frac{1}{\sqrt{2\pi \Sigma_2}} e^{-\frac{(x-\mu_2)^2}{2\Sigma_2}}
$$

$e^{-\frac{(x-\mu_1)^2}{2\Sigma_1}}$の$\mu_1$はベクトルなので$(x-\mu_1)^T(x-\mu_1)$となる

$$
log\ \frac{\frac{1}{\sqrt{2\pi \Sigma_1}} e^{-\frac{(x-\mu_1)^2}{2\Sigma_1}}}{ \frac{1}{\sqrt{2\pi \Sigma_2}} e^{-\frac{(x-\mu_2)^2}{2\Sigma_2}}} + log\ \frac{\pi_1}{\pi_2}\\
$$

$$
log\ \frac{|\Sigma_2|^{\frac{1}{2}}}{|\Sigma_1|^{\frac{1}{2}}}
 + log\ e^{{-\frac{(x-\mu_1)^T(x-\mu_1)}{2\Sigma_1}} - (- \frac{(x-\mu_2)^T(x-\mu_2)}{2\Sigma_2})} + log\ \frac{\pi_1}{\pi_2}
$$

$log\ e$の部分を計算すると

$$
\frac{1}{2}\Big( (x-\mu_2)^T \Sigma_2^{-1} (x-\mu_2) - (x-\mu_1)^T \Sigma_1^{-1} (x-\mu_1)\Big)\\
=\frac{1}{2} \Big( 
(x^T\Sigma_2^{-1}x 
- x^T\Sigma_2^{-1}\mu_2
- \mu_2^T\Sigma_2^{-1}x
- \mu_2^T\Sigma_1^{-1}\mu_2)\\

- (x^T\Sigma_1^{-1}x 
- x^T\Sigma_1^{-1}\mu_1
- \mu_1^T\Sigma_1^{-1}x
- \mu_1^T\Sigma_1^{-1}\mu_1)
 \Big)
$$

計算すると

$$
f(x) = x^T (-\Sigma^{-1}_1  + \Sigma_2^{-1}/2)x \\
+ (\Sigma^{-1}_1\mu_1 - \Sigma_2^{-1}\mu_2)^Tx\\
 + \frac{1}{2}(\mu^T \Sigma^{-1}_2 \mu_2 = \mu_1^T \Sigma^{-1} \mu_1)+ log\ \frac{|\Sigma_2|^{\frac{1}{2}}}{|\Sigma_1|^{\frac{1}{2}}} + log \frac{\pi_1}{\pi_2}
$$

- (2)
    省略