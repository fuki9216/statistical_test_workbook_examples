## 統計検定準1級(Statistical Test Pre-1st grade)
## 4章 例題1
### 参考

https://qiita.com/tarantula426/items/8b8e9bff11aca418e01d#1%E5%A4%89%E6%95%B0%E3%81%AE%E7%A2%BA%E7%8E%87%E5%AF%86%E5%BA%A6%E9%96%A2%E6%95%B0%E3%81%AE%E5%A4%89%E6%95%B0%E5%A4%89%E6%8F%9B

### 回答

- (1)
    
    期待値
    
    正規分布のモーメント母関数を用いて
    
    $$
    M_X(\theta ) = E[e^{\theta X}] = exp \Big(\theta\mu + \frac{\theta^2 \sigma^2}{2}\Big)
    $$
    
    $\theta=1$ とすると $e^X$ の期待値となる
    
    $$
    E[Y] = E[e^X] = M_X(1) = exp\Big( \mu + \frac{\sigma^2}{2}\Big)
    $$
    

- (2)
    
    分散
    
    $E[Y^2]$ は $\theta = 2$ として
    
    $$
    E[Y^2] = E[e^{2X}] = M_X(2) = exp\Big(2\mu + \frac{2^2\sigma^2}{2} \Big)\\
    = exp\Big(2\mu +2\sigma^2 \Big)
    $$
    
    $$
    V[Y] = exp\Big(2\mu +2\sigma^2 \Big) - exp\Big(2( \mu + \frac{\sigma^2}{2})\Big)\\
    共通項を括って\\
    = exp(2\mu + \sigma^2 )(exp(\sigma^2)-1)
    $$
    
- (3)
    
    確率密度関数
    
    変数変換の公式より
    
    $exp(X)$ を微分しても$exp(X)$ となるので
    
    $$
    \frac{1}{\sqrt{2\pi }\sigma}exp\Big( -(x-\mu)/2\sigma^2 \Big)\cdot \frac{1}{exp(X)}
    $$
    
    問題文より
    
    $$
    Y = exp(X)\\
    X = log(Y)
    $$
    
    こちらを代入すると
    
    $$
    \frac{1}{y\sqrt{2\pi }\sigma}exp\Big( -(log(y)-\mu)/2\sigma^2 \Big)
    $$