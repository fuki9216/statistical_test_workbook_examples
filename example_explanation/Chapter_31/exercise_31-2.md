### 回答

- (1)
    
    事前分布$G(2,1/3)$
    
    $\sum x = 15$
    
    $n =5$
    
    より
    
    事後分布$G(17, 1/8)$
    
    確率密度関数は
    
    $f(x) = \frac{b^a}{\Gamma(a)}x^{a-1} e^{-xb)}$より
    
    $$
    \frac{8^{17}}{\Gamma(17)}x^{17-1} e^{-8x}\\
    = \frac{8^{17} \lambda^{16} e^{-8\lambda}}{\Gamma(17) }
    $$
    
- (2)
    
    $$
    \int^{\infty}_0 f(x_6|\lambda) \pi(\lambda | x) d\lambda\\
    $$
    

$f(x_6|\lambda)$ ：6日目の確率密度関数PDF→$\frac{\lambda^{x_6} e^{-\lambda}}{x_6!}$

$\pi(\lambda | x)$ ：5日までのPDF→ $\frac{8^{17} \lambda^{16} e^{-8\lambda}}{\Gamma(17) }$

$$
\int^{\infty}_0  \frac{\lambda^{x_6} e^{-\lambda}}{x_6!}\frac{8^{17} \lambda^{16} e^{-8\lambda}}{\Gamma(17) }d\lambda\\
= \int^{\infty}_0 \frac{8^{17}\cdot \lambda^{x_6+16}\cdot  e^{-9\lambda}}{x_6!\ \Gamma(17)}\\
= 8^{17} \frac{\int^{\infty}_0\lambda^{x_6+16}\cdot  e^{-9\lambda}}{x_6!\ \Gamma(17)}
$$

$\int^{\infty}_0\lambda^{x_6+16}\cdot  e^{-9\lambda}$の計算

以下2パターンのどちらかに変換できる

- $\Gamma(a) = \int^{\infty}_0x^{a-1}\cdot  e^{-x}dx$
- $\frac{\Gamma(a)}{b^a} = \int^{\infty}_0x^{a-1}\cdot  e^{-bx}dx$

よって

$$
\int^{\infty}_0\lambda^{x_6+16}\cdot  e^{-9\lambda}\\
=\frac{\Gamma(x_6 + 17)}{9^{x_6 + 17}}
$$

$$
\frac{8^{17} }{x_6!\ \Gamma(17)} \frac{\Gamma(x_6 + 17)}{9^{x_6 + 17}}\\
= \frac{\Gamma(x_6 + 17)}{x_6!\ \Gamma(17)}(\frac{8}{9})^{17} (\frac{1}{9})^{x_6}
$$

この形は負の二項分布