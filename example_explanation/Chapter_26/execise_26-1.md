## 統計検定準1級(Statistical Test Pre-1st grade)
## 26章 例題1

### 計量MDSの手順
1. 距離行列Dを準備
2. 二重中心化して行列Bを作成
    
    $$
    B = -\frac{1}{2} (I_n - \frac{1}{n} J_n)D (I_n - \frac{1}{n} J_n)
    $$
    
    $I_n$：対角が1の単位行列
    
    $J_n$：全てが1の行列
    
3. Bの固有値、固有ベクトルを求める
    
    $|B - \lambda I| = 0$
    
4. 次元を選択し、固有値の大きい順に並べる
    
    固有値 $A = \begin{Vmatrix}
    \lambda_1&0\\
    0 & \lambda_2
    \end{Vmatrix}$,
    
    固有ベクトル $U=(u_1, u_2)$
    
5. 座標軸Xを求めて可視化する
    
    $X = UA^{\frac{1}{2}}$

### 回答
- (1)
    
    $$
    B = -\frac{1}{2}\Big( 
    \begin{Vmatrix}
    1&0&0&0\\
    0&1&0&0\\
    0&0&1&0\\
    0&0&0&1\\
    \end{Vmatrix}
    - \frac{1}{4} 
    \begin{Vmatrix}
    1&1&1&1\\
    1&1&1&1\\
    1&1&1&1\\
    1&1&1&1\\
    \end{Vmatrix}
     \Big)
    \begin{Vmatrix}
    0&5&5&16\\
    5&0&4&5\\
    5&4&0&5\\
    16&5&5&0\\
    \end{Vmatrix}
    \Big( 
    \begin{Vmatrix}
    1&0&0&0\\
    0&1&0&0\\
    0&0&1&0\\
    0&0&0&1\\
    \end{Vmatrix}
    - \frac{1}{4} 
    \begin{Vmatrix}
    1&1&1&1\\
    1&1&1&1\\
    1&1&1&1\\
    1&1&1&1\\
    \end{Vmatrix}
     \Big)\\
    $$
    
    計算すると
    
    $$
    \begin{Vmatrix}
    4&0&0&-4\\
    0&1&-1&0\\
    0&-1&1&0\\
    -4&0&0&4\\
    \end{Vmatrix}
    $$
    
    Bの固有値を解くと
    
    $$
    |B - \lambda I|= 0
    $$
    
    $$
    \Big|
    \begin{Vmatrix}
    4&0&0&-4\\
    0&1&-1&0\\
    0&-1&1&0\\
    -4&0&0&4\\
    \end{Vmatrix} - 
    \begin{Vmatrix}
    \lambda &0&0&0\\
    0&\lambda &0&0\\
    0&0&\lambda &0\\
    0&0&0&\lambda \\
    \end{Vmatrix}\Big|\\
     = \begin{Vmatrix}
    4-\lambda &0&0&-4\\
    0&1-\lambda &-1&0\\
    0&-1&1-\lambda &0\\
    -4&0&0&4-\lambda \\
    \end{Vmatrix}
    $$
    
    余因子展開を行う
    
    $$
    (4-\lambda )
    \begin{Vmatrix}
    1-\lambda &-1&0\\
    -1&1-\lambda &0\\
    0&0&4-\lambda \\
    \end{Vmatrix} 
    
    - 0 \begin{Vmatrix}
    0&-1&0\\
    0&1-\lambda &0\\
    -4&0&4-\lambda \\
    \end{Vmatrix}\\
    
    + 0 \begin{Vmatrix}
    0&1-\lambda &0\\
    0&-1&0\\
    -4&0&4-\lambda \\
    \end{Vmatrix}
    
    - (-4) \begin{Vmatrix}
    
    0&1-\lambda &-1\\
    0&-1&1-\lambda \\
    -4&0&0 \\
    \end{Vmatrix}\\
    
    = (4-\lambda )
    \begin{Vmatrix}
    1-\lambda &-1&0\\
    -1&1-\lambda &0\\
    0&0&4-\lambda \\
    \end{Vmatrix} 
    +4 \begin{Vmatrix}
    
    0&1-\lambda &-1\\
    0&-1&1-\lambda \\
    -4&0&0 \\
    \end{Vmatrix}
    $$
    
    行列式の計算$\begin{bmatrix}a & b\\ c& d \end{bmatrix} = ad- bc$ より
    
    $$
    (4-\lambda )\big[(1-\lambda)(1-\lambda) -(4-\lambda) \big]\\ - (-4)\big[(1-\lambda)(1-\lambda)(-4) - (-1)(-1)(-4) \big]\\
    = (4-\lambda)^2[ (1-\lambda)^2-1] - 16[(1-\lambda)^2 -1)]\\
    = [(1-\lambda)^2-1][(4-\lambda)^2-16]
    $$
    
    $[(1-\lambda)^2-1][(4-\lambda)^2-16]=0$ を解くとよって固有値は
    
    8，2，0，0
    
    $B=\begin{Vmatrix}
    4&0&0&-4\\
    0&1&-1&0\\
    0&-1&1&0\\
    -4&0&0&4\\
    \end{Vmatrix}$
    
    より
    
    $$
    \begin{Vmatrix}
    4-\lambda &0&0&-4\\
    0&1-\lambda &-1&0\\
    0&-1&1-\lambda &0\\
    -4&0&0&4-\lambda \\
    \end{Vmatrix}
    $$
    
    $\lambda = 8$：
    
    $$
    \begin{bmatrix}
    -4 & 0 & 0 & -4 \\
    0 & -7 & -1 & 0 \\
    0 & -1 & -7 & 0 \\
    -4 & 0 & 0 & -4
    \end{bmatrix}
    \begin{bmatrix} x \\ y \\ z \\ w \end{bmatrix}
    =
    \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix}
    $$
    
    1. $−4x−4w=0$
    2. $−7y−z=0$
    3. $-y - 7z = 0$
    4. $−4x−4w=0$
    
    よって$\begin{bmatrix} 1 \\ 0 \\ 0 \\ 1 \end{bmatrix}$　
    
    標準化（=1）するには
    
    $$
    \sqrt{a^2 + 0^2 + 0^2+ a^2} = 1\\
    \sqrt{2 a^2} =1 \\
    a = \sqrt{\frac{1}{2}}
    $$
    
    $$
    \begin{bmatrix} 
    \sqrt{\frac{1}{2}} \\ 0 \\ 0 \\ -\sqrt{\frac{1}{2}} \end{bmatrix}　
    $$
    
- (2)
    
    次元を1とした場合の座標X
    
    第1固有ベクトル8の場合のXは
    
    $X = UA^{\frac{1}{2}}$ より
    
    $$
    \begin{bmatrix} 
    \sqrt{\frac{1}{2}} \\ 0 \\ 0 \\ -\sqrt{\frac{1}{2}} \end{bmatrix}　
    \cdot \sqrt{8}
    = 
    \begin{bmatrix} 
    \sqrt{\frac{1}{2}} \\ 0 \\ 0 \\ -\sqrt{\frac{1}{2}} \end{bmatrix}　
    \cdot 2\sqrt{2}
    = 
    \begin{bmatrix} 
    2 \\ 0 \\ 0 \\ -2\end{bmatrix}　
    $$
    
    この距離行列を求めると
    
    $$
    \begin{bmatrix} 
    (2-2)^2 & (2-0)^2 & (2-0)^2 & (2-(-2))^2\\
    (0-2)^2 & (0-0)^2 & (0-0)^2 & (0-(-2))^2\\
    (0-2)^2 & (0-0)^2 & (0-0)^2 & (0-(-2))^2 \\
    (-2-2)^2 & (-2-0)^2 & (-2-0)^2 & (-2 - (-2))^2
    \end{bmatrix}\\　
    \begin{bmatrix} 
    0 & 4 & 4 & 16\\
    4 & 0 & 0 & 4\\
    4 & 0 & 0 & 4\\
    16 & 4 & 4 & 0
    \end{bmatrix}\\　
    $$
    
    Dと一致して無いので再現できていない
    
- (3)
    
    次元を2とした場合の$X = UA^{\frac{1}{2}}$は
    
    $$
    \begin{bmatrix} 
    \sqrt{\frac{1}{2}} & 0 \\
     0  & \sqrt{\frac{1}{2}}\\
     0  & -\sqrt{\frac{1}{2}}\\
     -\sqrt{\frac{1}{2}} & 0
    \end{bmatrix}　
    
    \begin{bmatrix} 
    \sqrt{8} & 0\\
    0 & \sqrt{2}
    \end{bmatrix}\\
    = 
    \begin{bmatrix} 
    2 & 0\\
    0 & 1\\
    0 & -1\\
    -2 & 0
    \end{bmatrix}\\
    $$
    

距離行列を計算すると

$$
\begin{bmatrix} 
(2-2)^2 + (0-0)^2 & (2-0)^2+ (0-1)^2& (2-0)^2+ (0-(-1))^2 & (2-(-2))^2 + (0-0)^2\\
(0-2)^2+ (1-0)^2 & (0-0)^2 + (1-1)^2 & (0-0^2 + (1-(-1))^2 & (0-(-2)^2 + (-1-0)^2\\
(0-2)^2 + (-1-0)^2 & (0-0)^2 + (-1-1)^2 & (0-0)^2 + (-1- (-1))^2 & (0-(-2) )^2 + (-1-0)^2\\
(-2-2)^2 + (0-0)^2 & (-2 -2)^2 + (0-0)^2 & (-2- 0)^2 + (0-(-1))^2 & (-2 -(-2))^2 + (0-0)^2
\end{bmatrix}\\
= 
\begin{bmatrix} 
0 & 5 & 5 & 16\\
5 & 0 & 4 & 5 \\
5 & 4 & 0 & 5\\
16 & 5 & 5 & 0
\end{bmatrix}\\
$$

Dと一致するので再現できている