## 統計検定準1級(Statistical Test Pre-1st grade)
## 8章 例題3
### 回答

- (1)
    
    対数尤度関数を求める
    
    $$
    L(\lambda) = \prod^n_{i=1}\frac{\lambda^{x_i} e^{-\lambda}}{x_i !}\\
    $$
    
    $\lambda$ が関わらない $x_i!$ を除外する
    
    $$
    = \prod^n_{i=1}\lambda^{x_i} e^{-\lambda}\\
    $$
    
    対数を取る
    
    $$
    = log\ \lambda^{\sum^n_{i=1}x_i} + log\ e^{-\lambda \cdot n}\\
    = \sum^n_{i=1}x_i \cdot log\ \lambda -n \lambda 
    $$
    
    $\lambda$ で微分して $=0$ とする
    
    $$
    -n +\frac{\sum^n_{i=1}x_i}{\lambda } = 0\\
    \lambda = \frac{\sum^n_{i=1}x_i}{n}
    $$
    
    よって$x$の平均となる
    
- (2)
    
    フィッシャー情報量について
    
    スコア関数：対数尤度を偏微分したもの
    
    $$
    S = \frac{\partial}{\partial  \theta}  log\ L(\theta|x)
    $$
    
    フィッシャー情報量$I(\lambda)$：
    
    1. スコア関数の分散(スコア関数の期待値は0)：$V\big[\frac{\partial}{\partial \theta} L(\theta|x) \big]$
    2. 対数尤度関数の2回微分した期待値の負：$-E\big[ \frac{\partial^2}{\partial  \theta^2}  log\ L(\theta|x) \big]$
    
    対数尤度を2回微分した値は
    
    1回微分した結果： $-n +\sum^n_{i=1}x_i \ \cdot \lambda^{-1}$ 
    
    2回微分した結果：$-1\cdot \sum^n_{i=1}x_i\cdot \lambda^{-2}= -\sum^n_{i=1}x_i\cdot \lambda^{-2}$ 
    
    $-E\big[ \frac{\partial^2}{\partial  \theta^2}  log\ L(\theta|x) \big]$を計算する
    
    $$
    -E\big[ \frac{\partial^2}{\partial  \theta^2}  log\ L(\theta|x) \big]\\
    = -E[-\sum^n_{i=1}x_i\cdot \lambda^{-2}]\\
    = E[\frac{\sum^n_{i=1}x_i}{ \lambda^{-2}}]\\
    = \sum^n_{i=1}E[\frac{x_i}{\lambda^{-2}}]\\
    =  \sum^n_{i=1}\frac{E[x_i]}{\lambda^{-2}}\\
    
    $$
    
    ポアソン分布の $E[x_i]$ は $\lambda$ なので
    
    $$
    =  \sum^n_{i=1}\frac{\lambda}{\lambda^{-2}}\\= \frac{n\lambda}{\lambda^2}= \frac{n}{\lambda}
    $$
    
- (3)
    
    クラメール・ラオの不等式$V[\lambda] \ge \frac{1}{I(\lambda)}$ を満たせば有効推定量といえる
    
    1より標本平均が最尤推定量となり、平均$\lambda$の不偏推定量となる
    
    $$
    V[\lambda] = V[\frac{\sum^n_{i=1} x_i}{n}]=\frac{1}{n^2} \sum^n_{i=1} V[x_i]\\
    V[x_i] = \lambdaより\\
    = \frac{1}{n^2} n\lambda= \frac{\lambda}{n}
    $$
    
    $$
    V[\lambda] \ge \frac{1}{I(\lambda)}\\
    \frac{n}{\lambda} = \frac{n}{\lambda}
    $$
    
    となるため、最尤推定量$\frac{\sum^n_{i=1}x_i}{n}$は有効推定量である
    
- (4)
    - 漸近正規性：サンプルサイズが無限に$\infty$
        
        $\hat{\lambda}$ $\hat{\lambda}$$\sqrt{n}(\hat{\lambda} - \lambda)→N(0, V(\hat{\lambda}))$の正規分布に収束する
        
        最尤推定量は(1)より $\hat{\lambda} = \sum^n_{i=1}x_i/n =\bar{X}$
        
        これより中心極限定理を適応して以下に収束する
        
        $$
        \sqrt{n}(\bar{X}- \lambda) →N(0, \lambda)
        $$
        
        よってこの最尤推定量は漸近正規性がある
        
    - 漸近有効性：最尤推定量 $\hat{\lambda}$ の分散がクラメール・ラオの不等式の下限に一致する場合、最尤推定量は漸近有効である
        
        (3)よりフィッシャー情報量$I(\lambda) = \frac{\lambda}{n}$ より、サンプルサイズが$\infty$ となるとき、$\lambda$ となる
        漸近正規性より分散は$\lambda$ と一致しているので、漸近有効性が示される