## 統計検定準1級(Statistical Test Pre-1st grade)
## 7章 例4
### 回答

デルタ法を用いる

- デルタ法：
    
    ある関数を $f$ を用いて $f(\bar{X_n})$ と表されてる量を考える
    
    $f(x)$ が連続微分可能な時、$\sqrt{n}\big(f(\bar{X_n})-f(\mu)\big)$ は $N\big(0, f'(\mu)^2\sigma^2 \big)$ に収束する
    

$\sqrt{n} \big(\bar{X}_n^2 - \mu^2 \big)$ の収束分布を求める

$f(x) = x^2$ とすると

$$
Z = \sqrt{n}(\bar{X}^2 - \mu^2) = \sqrt{n}\big(f(\bar{X})- f(\mu)\big)
$$

よりデルタ法を用いて

$$
N(0, f'(\mu)^2\sigma^2)\\
= N(0, (2\mu)^2 \sigma^2)
$$

となる

- 詳細の計算
    
    テイラー展開の一次近似を用いて
    
     $f(X)\approx f(\mu) + \frac{f'(\mu)}{1!}(X- \mu)$ 
    
    ↓変換して
    $f(X)- f(\mu) = f'(\mu)(X - \mu)$
    
    より
    
    $$
    \sqrt{n}\big(f(\bar{X})- f(x)\big) = \sqrt{n}\big( f'(\mu)(\bar{X} - \mu) \big)\\
    
    $$
    
    中心極限定理 $\sqrt{n}(\bar{X}- \mu) \approx N(0, \sigma^2)$ より
    
    $$
    \sqrt{n}\big( f'(\mu)(\bar{X} - \mu) \big) \approx N(0,f'(\mu)^2 \sigma^2)
    $$
    
    $f'(x) = 2x$ より $f'(\mu) = 2\mu$
    
    よって $N(0,(2\mu)^2\sigma^2 )$ に収束する