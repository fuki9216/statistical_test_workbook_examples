## 統計検定準1級(Statistical Test Pre-1st grade)
## 8章 例3
### 回答
モーメントを利用する

1次モーメント：$E[X]$で期待値を表し、確率分布の重心を表す

$$
\mu_1 = E[X]
$$

2次モーメント：2次モーメント自体は$E[X^2]$だが、通常は中心化されたモーメント
$V[X] = E(X-E[X]^2)$を利用する

$$
\mu_2 = E[(X-E[X])^2]
$$

$Ga(\alpha, \frac{1}{\lambda})$の平均と分散

$$

E[X] = \frac{\alpha}{\lambda}\\
V[X] = \frac{\alpha}{\lambda^2}\\

$$

標本の1次、2次モーメントを計算

$$

\bar{X} = \frac{1}{n}\sum^n_{i=1} X_i\\
S^2 = \frac{1}{n} \sum^n_{i=1}(X_i - \bar{X})^2
$$

モーメント法ではモーメントと標本モーメントを一致させる

1次モーメント

$$

\frac{\alpha}{\lambda} = \bar{X}\\

$$

2次モーメント

$$
\frac{\alpha}{\lambda^2} = S^2\\
$$

2つの連立方程式を解くと

$$
\alpha = \frac{\bar{X}^2}{S^2}\\
\lambda = \frac{\bar{X}}{S^2}
$$