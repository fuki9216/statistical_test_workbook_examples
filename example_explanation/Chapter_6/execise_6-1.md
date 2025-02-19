## 統計検定準1級(Statistical Test Pre-1st grade)
## 6章 例題1

### 回答

- (1)
    
    Aくん：70
    
    Bくん：45
    
- (2)
    
    $Z$ 値が $-0.5〜2$ の間は
    
    下側：0.3085 
    
    上側：0.0228
    
    この間は$0.6687$ なので669人
    
- (3)
    
    標準正規分布のZ値が $0.25\%$ の点は $0.675$ なので
    
    $$
    0.675\cdot 10\cdot 2 = 13.5
    $$
    
- (4)
    
    0以上で積分するが、
    
    確率密度の条件付き期待値を利用する
    
    $$
    E[Z|Z\geq 0]=\frac{\int^{\infty}_0 z f(z) dz}{P(Z\geq 0)}
    $$
    
    $P(Z\geq 0)$ ： $1/2$ より
    
    $$
    \frac{\int^{\infty}_0 x \cdot \frac{1}{\sqrt{2 \pi}} exp(\frac{-z^2}{2})}{1/2}\\
    = \frac{2}{\sqrt{2 \pi}}\int^{\infty}_0 z \cdot exp(- \frac{1}{2} z^2)\\
    
    $$
    
    ガウス積分を適応する
    
    $\int^{\infty}_0 xe^{-ax^2} = \frac{1}{2a}$ 
    
    $$
    = \frac{2}{\sqrt{2 \pi}}\cdot \frac{1}{2 \cdot \frac{1}{2}}\\= 0.79...
    $$
    
    標準偏差10と掛けて
    
    $$
    65+7.9..= 72.9..
    $$
    
### ガウス積分

https://manabitimes.jp/math/754

全範囲の積分

$$
\int^{\infty}_\infty e^{-ax^2} = \sqrt{\frac{\pi}{a}}\\

\int^{\infty}_\infty x \cdot e^{-ax^2} = 0\\

\int^{\infty}_\infty x^2 \cdot e^{-ax^2} = \frac{1}{2}\sqrt{\frac{\pi}{a^3}}\\

\int^{\infty}_\infty x^3 \cdot e^{-ax^2}  = 0
$$

0以上の積分

$$
\int^{\infty}_0 e^{-ax^2} = \frac{1}{2} \sqrt{\frac{\pi}{a}}\\

\int^{\infty}_0 x \cdot e^{-ax^2} = \frac{1}{2a}\\

\int^{\infty}_0 x^2 \cdot e^{-ax^2} = \frac{1}{4}\sqrt{\frac{\pi}{a^3}}\\

\int^{\infty}_0 x^3 \cdot e^{-ax^2}  = \frac{1}{2a^2}
$$