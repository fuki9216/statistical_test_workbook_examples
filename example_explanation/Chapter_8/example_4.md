## 統計検定準1級(Statistical Test Pre-1st grade)
## 8章 例4
### 参考

https://qiita.com/Isaka-code/items/9907955bf34c49df5bdd#%E7%A2%BA%E7%8E%87%E5%88%86%E5%B8%83%E3%81%AE%E7%A2%BA%E8%AA%8D-1

### 回答

- 十分統計量：データの情報を失わずにパラメータを要約できる統計量
    
    求め方
    
    1. 尤度関数を求める
        
        $L(\theta|X) = \prod^n_{i=1} f(X_i|\theta)$ 
        
    2. ネイマン・フィッシャーの分解定理を適用
        
        $$
        L(\theta|X) = g\big(T(X),\theta \big)h(X)
        $$
        
        - $g(T(X),\theta)$ ：$\theta$ に依存し、 $T(X)$ が無いと計算できない関数
        - $h(X)$ ： $\theta$ に依存しない関数
        
        この形に分解できる時、 $T(X)$ は十分統計量である
        

尤度関数

$$
L(\mu, \sigma^2|X) = \prod^n_{i=1} f(X_i|\mu, \sigma^2)\\

= \prod^n_{i=1} \frac{1}{\sqrt{2\pi \sigma^2}} exp\big( - \frac{(X - \mu)^2}{2\sigma^2}  \big)\\

$$

計算すると

$$
= \big( \frac{1}{\sqrt{2\pi \sigma^2}}\big)^n exp\big( - \frac{1}{2\sigma^2} \sum^n_{i=1} (X - \mu)^2 \big)\\

= \big( \frac{1}{\sqrt{2\pi \sigma^2}}\big)^n exp(-\frac{n\mu^2 - 2\mu \sum^n_{i=1}x_i + \sum^n_{i=1} x_i^2}{2\sigma^2})\\

= \big( \frac{1}{\sqrt{2\pi \sigma^2}}\big)^n exp
\big( 
-\frac{n\mu^2}{2\sigma^2}
+\frac{\mu \sum^n_{i=1}x_i}{\sigma^2}
-\frac{\sum^n_{i=1}x^2_i}{2\sigma^2}
\big)\\

$$

$= h(x) g(T(X), \theta)$ の形になっている

フィッシャーネイマンの分解定理を用いて導出する

$$
L(\mu, \sigma^2, X) = g(T(X), \mu, \sigma^2)\cdot h(X)
$$

- $T(X)$：十分統計量
- $g(T(X), \mu, \sigma^2)$：パラメータ$\mu, \sigma^2$に依存
- $h(X)$：$X$のみに依存

$\mu, \sigma^2$ が未知のとき、

$T_1 = \sum^n_{i=1} x_i$

$T_2 = \sum^n_{i=1} x_i^2$

とすると

$$
g(T_1, T_1; \mu, \sigma^2) = (\frac{1}{\sqrt{2\pi\sigma^2}})^n exp(-\frac{n\mu^2 - 2\mu T_1 + T_2}{2\sigma^2})
$$

$h(x_1, x_2,...x_n)=1$

のように表現でき、$\sum^n_{i=1} x_i, \sum^n_{i=1} x_i^2$ が十分統計量になる