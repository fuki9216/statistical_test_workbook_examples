## 統計検定準1級(Statistical Test Pre-1st grade)
## 15章 例題1
### 回答

$$
Z_t =  X_{t \Delta} - X_{(t-1)\Delta}\\
 = \sigma(B_t - B_{t-1}) 〜N(0,\sigma^2 \Delta)に従う
$$

$n$：100（分割した数）

$\Delta$：1（$\frac{1}{100}$とするため）

上記を置くことで、パラメータ推定公式

$$
\frac{1}{n} \sum^n_{k=1} Z_k = \hat{\mu}\Delta \\
\frac{1}{n} \sum^n_{k=1} Z_k^2 = \hat{\sigma}^2\Delta + (\hat{\mu} \Delta)^2
$$

を利用することができる

今回は$\hat{\mu} \Delta$は0とする

- (1)
    
    $\Delta = 1$とおいて
    
    $$
    \hat{\sigma^2}\Delta = V = 0.0225
    $$
    
    $V = \sigma^2$ より、
    
    $$
    \sigma = \sqrt{0.0225} = 0.15
    $$
    
- (2)
    
    $\Delta = \frac{1}{10}$とおいて
    
    $$
    \hat{\sigma}^2\Delta = V_1 = 0.00625\\
    \sigma^2 = 0.0625\\
    \sigma = 0.25
    $$