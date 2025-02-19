## 統計検定準1級(Statistical Test Pre-1st grade)
## 6章 例題3

### 回答
- (1)
    
    生存関数について
    
    $$
    累積分布関数：F(t) = 1-S(t)
    $$
    
    累積分布関数を微分すると確率密度関数を求められる
    
    $$
    F(t) = 1-exp(-\lambda t)
    $$
    
    $$
    F'(x) = f(x)\\
     = -(-\lambda)exp(-\lambda t)\\ =\lambda \ exp(- \lambda t)
    $$
    
- (2)
    - 期待値
        
        期待値を求めるには以下の積分を求める必要がある
        
        $$
        \int^{\infty}_0 t \cdot \lambda \ exp(- \lambda t) dt\\
        $$
        
        $f(x) = t$ 
        
        $G(x) = \int \lambda\ exp(-\lambda t) = \lambda /-\lambda exp(-\lambda t)=- exp(-\lambda t)$
        
        部分積分の公式： $\int f(x)\ g(x) = f(x) G(x) - \int f'(x)\ G(x)$ 
        
        より
        
        $$
        [t\cdot - exp(-\lambda t)]^\infty_0 - \int^\infty_0 -exp(-\lambda t)dt\\
        = [t\cdot - exp(-\lambda t)]^\infty_0 + \int^\infty_0 exp(-\lambda t)dt\\
        $$
        
        ここで
        
        $$
        [t\cdot - exp(-\lambda t)]^\infty_0\\
        = 0 - (-0\cdot 1)=0
        $$
        
        $$
        \int^\infty_0 exp(-\lambda t)dt\\
        = [\frac{1}{-\lambda} exp(-\lambda t)]^\infty_0\\
        = 0 - (-\frac{1}{\lambda})\\
        = \frac{1}{\lambda}
        $$
        
        より期待値は
        
        $$
        \frac{1}{\lambda}
        $$
        
    - 上側25%点
        
        $P(T>t) = 0.25$ を満たす $t$ を求める
        
        すなわち $S(t) =exp(-\lambda t)= 0.25$ を満たす必要があるので
        
    
    $$
    
    ext(-\lambda t) = \frac{1}{4}\\
    -\lambda t = log\ \frac{1}{4}\\
    -\lambda t = log1 - log 4\\
    -\lambda t = 0 - log 4\\
    t = \frac{log 4}{\lambda}
    
    $$
    

(3)

$$
\frac{1}{\lambda} = 3より\\
\lambda = \frac{1}{3}\\

\frac{log 4}{\lambda } = log4\cdot  \frac{3}{1} \\
= 4.2年
$$