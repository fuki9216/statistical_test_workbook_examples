## 統計検定準1級(Statistical Test Pre-1st grade)
## 2章 例題2-2

### 参考

https://note.com/ebikazuki/n/n0ace45d1cf6a#79c6f57c-74c8-4be1-8213-b7f34d863fad

### 回答

- 確率母関数
    
    $$
    G(s) = \sum s^x p(x)\\
    = \sum s^x p(1-p)^x\\
    = p \sum s^x (1-p)^x\\
    = p \sum (s (1-p))^x\\
    ここで、|a|が1より小さい時、\\
    \sum a^x = \frac{1}{1-a}より\\
    
    = p \cdot \frac{1}{1-(s(1-p))}\\
    = \frac{p}{1-(s(1-p))}
    $$
    
- 期待値
    
    指数関数の微分公式より
    
    $$
    [g(s)^{x}]′ = x \cdot g'(s) \cdot g(s)^{x-1}
    $$
    
    $$
    E[x]\\
    =p \cdot \frac{d}{dx} [1-s(1-p)]^{-1}\\
    = p \cdot (1- p) [1-s(1-p)]^{-2}\\
    s=1を代入する\\
    = p \cdot -(-(1- p)) \cdot [1-(1-p)]^{-2}\\
    = p \cdot (1- p) \cdot p^{-2}\\
    = \frac {p \cdot (1- p)}{p^{2}}\\
    = \frac {1- p}{p}\\
    $$
    
- 分散
    
    分散は2回微分して $s=1$ を代入すると
    
     $G''(1) = E[X(X-1)]$ 
    
    となるので、
    
    $$
    V[X]\\
    = E[X^2] - E[x]\\
    =E[X^2] - E[X] +E[X] -(E[X])^2\\
    = G''(1)+ G'(1) - (G'(1))^2\\
    
    $$
    
    $G''(1)$  を求めると
    
    $$
    \frac{\partial}{\partial s}p(1-p)(1-s(1-p))^{-2}\\
    = p(1-p)\frac{\partial}{\partial s}(1-s(1-p))^{-2}\\
    = p(1-p)(-2)(1-s(1-p))^{-3}(-(1-p))\\
    =\frac{ 2p(1-p)^2}{(1-s(1-p))^3}\\
    = \frac{ 2p(1-p)^2}{p^3}\\
    = \frac{ 2(1-p)^2}{p^2}\\
    $$
    
    よって分散 $V[X]$ は
    
    $$
    = \frac{2(1-p)^2}{p^2} + \frac{1-p}{p}-(\frac{1-p}{p})^2 \\
    =\frac{2(1-p)^2 +p(1-p)-(1-p)^2}{p^2}\\
    = \frac{(1-p)^2+p(1-p)}{p^2}\\
    = \frac{(1-p)((1-p)+p)}{p^2}\\
    =\frac{1-p}{p^2}
    $$