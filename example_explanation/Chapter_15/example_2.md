## 統計検定準1級(Statistical Test Pre-1st grade)
## 15章 例2
### 回答

- 複合ポアソン過程
    
    例：地震に対する損害額
    
    $$
    S(t) = \sum_{i=1}^{N(t)} U_i
    $$
    
    $N(t)$：ポアソン過程
    
    $U_i$：ポアソン過程発生時における総被害額のモデル
    

$X$：$X_t = \sum_{k=1}^{N(t)} U_k$の複合ポアソン過程とする

$N(t)$は$t$時点までのポアソン過程で、強度$\lambda$のポアソン分布に従う

$E[N_t] = \lambda t$

$U_t$は独立同分布に従うランダム変数で、各時点での発生する値

$E[U_k] = \mu$

$V[U_k] = \sigma^2$

- (1)
    
    基本事項
    
    - $E[X_t]$
        
        以下に変換できる
        
        $$
        E[X_t] = E\big[ \sum_{k = 1}^{N(t)} U_t \big]
        $$
        
        $N_t$が確率変数のため条件付き期待値を導入する
        
        $N(t)$が$n$回と与えられた時の条件付き期待値
        
        $$
        E \Big[ \sum_{k=1}^{N(t)} U_k| N(t) = n \Big]\\
        条件付期待値にするとN(t)を置き換えられる\\
        = \sum_{k=1}^n E[U_k] = n \mu
        $$
        
        $E[X_t]$全体で見るとすべての$N_t$に対して期待値の重み付け平均として表現できる
        
        $$
        E[X_t] = E\big[E[X_t| N(t)] \big]\\
        = E\big[E[\sum_{k =1}^{N(t)} U_k| N(t)] \big]\\
        N(t)の場合の条件付き期待値を代入する\\
        = E \big[ N(t) \mu \big]\\
        = \mu\cdot E[N(t)]\\
        = \mu \cdot \lambda t\\
        = \lambda \mu t
        $$
        
    - $V[X_t]$
        
        $V[X_t] = E[X_t^2] - (E[X_t])^2$を考える
        
        $E[X_t^2]$から計算する
        
        $$
        E[X_t^2] = E\Big[(\sum_{k=1}^{N(t)} U_t)^2\Big]\\
        和の二乗公式を用いて\\
        E\Big[ \sum_{k=1}^{N(t)}U_k^2 + 2 \sum_{1\le i \le j \le n} U_i U_j \Big]\\
        
        $$
        
        $i,j$は独立なので$E[U_i U_j] = E[U_i]\cdot E[U_j]$が成り立つことを考慮して
        
        $N(t) = n$と固定すると
        
        $$
        E[X_t^2 | N(t) = n] = \sum_{k=1}^n E[U_k^2] + 2 \sum_{1\le i \le j \le n} E[U_i]\cdot E[U_j]\\
        $$
        
        $\sum_{1\le i \le j \le n}$は重複を除く全ペアの和なので${}_nC_2 = \frac{n!}{(n-2)! \cdot 2!} = \frac{n(n-1)}{2}$ 通りある
        
        $E[U_k^2] = V[U_k] + (E[U_k])^2 = \sigma^2 + \mu^2$ より
        
        $$
        E[X_t^2 | N(t) = n] =\sum_{k=1}^n(\sigma^2 + \mu^2) + 2 \cdot \frac{n(n-1)}{2} \mu^2\\
        = n(\sigma^2 + \mu^2) + {n(n-1)} \mu^2\\
        = n\sigma^2 + n^2 \mu^2
        $$
        
        よって
        
        $$
        E[X_t^2] = E\Big[ N_t \sigma^2 + N_t^2 \mu^2 \Big]\\
        = E[N_t]\cdot E[\sigma^2] + E[N_t^2] \cdot E[\mu^2]\\
        $$
        
        $E[N_t] = \lambda t$ 
        
        $V[N_t] = \lambda t$  (ポアソン分布の性質より)
        
        $E[N_t^2]= V[N_t] + (E[N_t])^2 = \lambda t + (\lambda t)^2$ を用いて
        
        $$
        E[X_t^2] = E[N_t]\cdot E[\sigma^2] + E[N_t^2] \cdot E[\mu^2]\\
        = \lambda t \sigma^2 + \mu^2 (\lambda t + (\lambda t)^2)
        $$
        
        $$
        V[X_t] = E[X_t^2] - (E[X_t])^2\\
        = \lambda t \sigma^2 + \mu^2 (\lambda t + (\lambda t)^2) - (\lambda \mu t)^2\\
        = \lambda t \sigma^2 + \lambda t \mu^2 + \lambda^2 t^2 \mu^2 - \lambda^2 t^2 \mu^2 \\
        = \lambda t \sigma^2 + \lambda t \mu^2\\
        = \lambda t (\sigma^2 + \mu^2)
        $$
        

- (2)
    
    $$
    E\Big[e^{s X_t} \Big]  = E \Big[ e^{s \sum^{N_t}_{k=1} U_k} \Big]
    $$
    
    $N_t$が与えられた場合の条件付き期待値として$N_t$を固定する
    
    $$
    M_{X_t}(s) = E\Big[ E[e^{s \sum^{N_t}_{k=1} U_k}| N_t] \Big]
    $$
    
    $U_k$は互いに独立のため
    
    $$
    E\Big[ \prod^{N_t}_{k=1} E\big[ e^{s U_k}  \big] \Big] = E\Big[\prod^{N_t}_{k=1} \phi(s) \Big]\\
    = E\big[ \phi(s)^{N_t} \big]
    $$
    
    上記の期待値を求めるには確率と掛けて合計する加重平均を取る
    
    $N_t$はポアソン過程なので確率は
    
    $$
    p(N_t) = \frac{ (\lambda t)^{N_t} e^{-\lambda t}}{N_t!}
    $$
    
    上記を用いてモーメント母関数を計算する
    
    $$
    M_{X_t}(s) = \sum^{\infty}_{n=0}\phi(s)^{N_t} \cdot \frac{ (\lambda t)^{N_t} e^{-\lambda t}}{N_t!}
    $$
    
    無限和の公式$\sum^{\infty}_{n=0}\frac{(a\cdot b)^n}{n!} = e^{ab}$より
    
    $$
    M_{X_t}(s) = e^{-\lambda t} \cdot e^{\lambda t \phi (s)}\\
    = e^{\lambda t (\phi (s) - 1)}
    $$