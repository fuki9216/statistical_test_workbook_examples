## 統計検定準1級(Statistical Test Pre-1st grade)
## 14章 例題3
### 回答

- (1)
    
    状態空間$S$：それぞれの場所の傘の本数$[ 0, 1, 2]$
    
    初期分布$\pi_0$：最初はそれぞれに傘を1本ずつおいてスタートする
    
    家からスタートするとして、家には1本あり、それ以外は無いので、
    
    $$
    \pi_0 = \begin{bmatrix}
    0 & 1 & 0
    \end{bmatrix}
    $$
    
    状態推移確率$Q$ ：
    
    行：移動前の元いた場所の傘の本数
    列：移動後目的地の傘の本数
    
    $$
    Q = \begin{bmatrix}
    p(0→0) & p(0→1) & p(0→2) \\
    p(1→0) & p(1→1) & p(1→2) \\
    p(2→0) & p(2→1) & p(2→2) \\
    \end{bmatrix}\\
    = \begin{bmatrix}
    0 & 0 & 1(天候に関係なく2本ある状態)\\
    0 & 1-\theta(雨がふらない確率) & \theta(雨が降った確率)\\
    1-\theta(雨が振らなかったら)& \theta(雨が降ったら)& 0
    
    \end{bmatrix}\\
    = \begin{bmatrix}
    0 & 0 & 1\\
    0 & 1-\theta & \theta\\
    1-\theta& \theta& 0
    \end{bmatrix}\\
    $$
    
- (2)
    
    1→1→2→0→2→1→1→1
    
    上記の移動時にそれぞれ以下の確率となっている
    
    $1-\theta ,\theta ,1-\theta ,1,\theta, 1-\theta ,1-\theta$ 
    
    尤度関数
    
    $$
    L = \theta^2 \cdot (1-\theta)^4 \cdot 1
    $$
    
    対数尤度
    
    $$
    log\ L = 2 log \theta+ 4log(1-\theta)
    $$
    
    微分した結果が0になる$\theta$を求める
    
    $$
    \frac{\partial}{\partial \theta} = \frac{2}{\theta} - \frac{4}{(1-\theta)} = 0\\
    \frac{2(1-\theta) - 4\theta}{\theta (1-\theta)} = 0\\
    \theta = \frac{1}{3}
    $$
    
- (3)
    
    (2)より推移確率行列$Q$は
    
    $$
    Q= \begin{bmatrix}
    0 & 0 & 1\\
    0 & \frac{2}{3} & \frac{1}{3}\\
    \frac{2}{3}& \frac{1}{3} & 0
    \end{bmatrix}\\
    $$
    
    定常分布における0の確率を求める
    
    $$
    \pi Q = \pi\\
    \begin{bmatrix}
    a & b & c 
    \end{bmatrix}
    \begin{bmatrix}
    0 & 0 & 1\\
    0 & \frac{2}{3} & \frac{1}{3}\\
    \frac{2}{3}& \frac{1}{3} & 0
    \end{bmatrix} = \begin{bmatrix}
    a & b & c 
    \end{bmatrix}
    $$
    
    $$
    a + b + c = 1
    $$
    
    上記を計算すると
    
    $a = \frac{1}{4}$、$b = \frac{3}{8}$ 、$c = \frac{3}{8}$
    
    $$
    \begin{bmatrix}
    \frac{1}{4} & \frac{3}{8} & \frac{3}{8}
    \end{bmatrix}
    $$
    
    よって0の確率は $\frac{1}{4}$