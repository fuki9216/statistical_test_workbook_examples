## 統計検定準1級(Statistical Test Pre-1st grade)
## 2章 例題2-3

- モーメント母関数
    
    $$
    f(x) = \lambda e^{- \lambda x}\\
    $$
    
    モーメント母関数の求め方
    
    $$
    m(\theta)= \int^{\infty}_0 e^{x\theta} f(x)\ dx\\
    $$
    
    より
    
    $$
    \int^{\infty}_0 e^{\theta x}\ \lambda e^{-\lambda x}\\
    = \lambda \int^{\infty}_0 e^{x(\theta-\lambda)}dx\\
    = \lambda \int^{\infty}_0 e^{-(\lambda-\theta)x}dx\\
    $$
    
    $$
    \int e^{-b x} dx= \frac{1}{b}e^{bx}
    $$
    
    より
    
    $$
     \lambda \int^{\infty}_0 e^{-(\lambda-\theta)x}dx\\
    = \frac{\lambda}{\lambda -\theta}
    $$
    
- 期待値
    
    モーメント母関数を $\theta$ で微分して0を代入する
    
    $$
    \frac{\partial}{\partial \theta} \lambda (\lambda - \theta)^{-1}\\
    
    = \lambda \frac{\partial}{\partial \theta}(\lambda - \theta)^{-1}\\
    
    = \lambda \cdot -1 (\lambda -\theta)^{-2}(-1)\\
    = \lambda /(\lambda-\theta )^2
    $$
    
    $\theta = 0$ を代入して
    
    $$
    \frac{\lambda}{\lambda^2} = \frac{1}{\lambda}
    $$
    
- 分散
    
    分散を求めるには $V[X] = E[X^2] - (E[X])^2$ 
    $E[X^2]$ はモーメント母関数を2回微分して0を代入する
    
    $$
    \lambda (\lambda-\theta )^{-2}\\
    =\lambda (-2)(\lambda - \theta)^{-3}(-1)\\
    = \frac{2\lambda}{\lambda^3}\\
    = \frac{2}{\lambda^2}
    $$
    
    よって
    
    $$
    V[X] = \frac{2}{\lambda^2} - (\frac{1}{\lambda})^2\\
    = \frac{1}{\lambda^2}
    $$