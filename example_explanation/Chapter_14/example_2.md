## 統計検定準1級(Statistical Test Pre-1st grade)
## 14章 例2
### 回答

- $Q_1$
    
    $$
    Q=\begin{bmatrix}0 & \frac{1}{2} & \frac{1}{2} \\\frac{1}{2}  & 0 & \frac{1}{2} \\\frac{1}{2}  & \frac{1}{2}  & 0\end{bmatrix}
    $$
    
    $\pi = a,b,c$より
    
    $$
    \pi Q = (a,b,c)\begin{bmatrix}0 & \frac{1}{2} & \frac{1}{2} \\\frac{1}{2}  & 0 & \frac{1}{2} \\\frac{1}{2}  & \frac{1}{2}  & 0\end{bmatrix}\\
    $$
    
     
    
    $$
    a = \frac{1}{2}b +\frac{1}{2}c\\
    b = \frac{1}{2}a + \frac{1}{2}c\\
    c = \frac{1}{2}a + \frac{1}{2}c
    $$
    
    $a+b+c = 1$より
    
    $$
    2a = b + c\\
    a + 2a = 1\\
    a = \frac{1}{3}\\
    
    $$
    
    計算を進めると
    
    $$
    b = \frac{1}{3}\\
    c = \frac{1}{3}
    $$
    
    よって
    
    $$
    \pi = (\frac{1}{3}, \frac{1}{3}, \frac{1}{3})
    $$
    
    上記が確率分布である条件を満たし、一様分布となる
    
- $Q_2$
    
    $$
    Q=\begin{bmatrix}
    \frac{1}{3} & \frac{2}{3} & 0 \\\
    \frac{1}{3}  & \frac{1}{3} & \frac{1}{3} \\
    0 & 0 & 1
    \end{bmatrix}
    $$
    
    $$
    a⋅ 1/3 +b⋅ 1/3 +c⋅0=a\\
    a⋅ 2/3 +b⋅ 1/3 +c⋅0=b\\
    a⋅0+b⋅ 0 +c⋅1=c \\
    
    \frac{1}{3}a + \frac{1}{3}b = a\\
    \\
    \frac{2}{3}a + \frac{1}{3}b = b\\
    \frac{1}{3}b + c = c
    $$
    
    正規化条件
    
    $a+b+c=1$
    
    計算すると
    
    $$
    a=0\\
    b=0\\
    c=1
    $$
    
    この推移確率行列$Q$は吸収状態となっている（状態 3 に入るとそこから出られない）
    
    十分時間が経つと確率分布は状態 3 に完全に集中し、他の状態に確率が分布することは無い
    
    これより
    
    $$
    \pi = (0,0,1)
    $$
    
    の定常分布になる