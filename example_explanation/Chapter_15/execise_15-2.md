## 統計検定準1級(Statistical Test Pre-1st grade)
## 15章 例題2
### 回答

- (1)
    
    不良品の発生が稀な減少としたときに、累積数の増加が直線的になっているので$N_t$の強度は一定
    
    また、不良品の発生は独立のため、独立増分性を持つ
    
    そのため$N = (N_t)_{t\ge0}$を仮定することは妥当
    
- (2)
    
    $$
    \hat{\lambda} = \frac{イベントの総回数}{観測時間}
    $$
    
    より
    
    $$
    \frac{558}{300} = 1.86
    $$
    
- (3)
    
    15例2と同様の解き方を行う
    
    - $E[X_t]$
        
        以下に変換できる
        
        $$
        E[X_t] = E\big[ \sum_{k = 1}^{N(t)} U_k \big]
        $$
        
        $N_t$が確率変数のため条件付き期待値を導入する
        
        $N(t)$が$n$回と与えられた時の条件付き期待値
        
        $$
        E \Big[ \sum_{k=1}^{N(t)} U_k| N(t) \Big]\\
        条件付期待値にするとN(t)を固定する\\
        = E\Big[ \sum_{k=1}^{N_t} E[U_k] \Big] = E[N_t q]\\
        = E[N_t] q= \lambda t q
        $$
        
        $t= 1$より、$\lambda q$
        
    - $V[X_t]$
        
        $V[X_t] = E[X_t^2] - (E[X_t])^2$を考える
        
        $E[X_t^2]$から計算する
        
        $$
        E[X_t^2] = E\Big[(\sum_{k=1}^{N(t)} U_k)^2\Big]\\
        和の二乗公式を用いて\\
        E\Big[ \sum_{k=1}^{N(t)}U_k^2 + 2 \sum_{1\le i \le j \le n} U_i U_j \Big]\\
        
        $$
        
        $i,j$は独立なので$E[U_i U_j] = E[U_i]\cdot E[U_j]$が成り立つことを考慮して
        
        $N(t)$の条件付き期待として
        
        $$
        E[X_t^2 | N(t)] = \sum_{k=1}^{N_t} E[U_k^2] + 2 \sum_{1\le i \le j \le n} E[U_i]\cdot E[U_j]\\
        $$
        
        $\sum_{1\le i \le j \le n}$は重複を除く全ペアの和なので${}_nC_2 = \frac{n!}{(n-2)! \cdot 2!} = \frac{n(n-1)}{2}$ 通りある
        
        ベルヌーイ分布の期待値、分散から$E[U_k^2] = V[U_k] + (E[U_k])^2 = q(1-q) + q^2$ 
        
        $$
        E\Big[E[X_t^2 | N(t)] \Big]=E\Big [\sum_{k=1}^{N_t}(q(1-q) + q^2) + 2 \cdot \frac{N_t(N_t-1)}{2} q^2 \Big]\\
        = E\Big[ N_t(q(1-q) + q^2) + {N_t(N_t - 1)} q^2 \Big]\\
        = E\Big[ N_t q +N_t^2 q^2 - N_t q^2\Big]\\
        = E\Big[N_tq(1-q) +N_t^2 q^2 \Big]\\
        = E[N_t]q(1-q) + E[N_t^2] q^2\\
        
        $$
        
        $E[N_t^2] = V[N_t]+ (E[N_t])^2 = \lambda t + (\lambda t)^2$より
        
        $$
        = \lambda t \cdot g(1-q) + q^2(\lambda t + (\lambda t)^2)\\
        = \lambda t\ q + q^2 (\lambda t)^2
        $$
        
        $t=1$より$\lambda q + q^2\lambda^2$
        
        よって$V[X_1]$は
        
        $$
        V[X_1] = E[X_1^2] - (E[X_1])^2\\
        = \lambda q + q^2 \lambda^2 - (\lambda q)^2\\
        = \lambda q
        $$
        
- (4)
    
    差分を取ることで
    
    $$
    \frac{1}{n} \sum^n_{k=1} Z_k = \hat{\mu}\Delta \\
    \frac{1}{n} \sum^n_{k=1} Z_k^2 = \hat{\sigma}^2\Delta + (\hat{\mu} \Delta)^2
    $$
    
    を利用できる
    
    $\Delta = 1$として
    
    $$
    \hat{\mu} \Delta = 1\lambda q = 1.53\\
    1.86 q = 1.53\\
    q = 0.8225...
    $$