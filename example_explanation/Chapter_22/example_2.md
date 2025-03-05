## 統計検定準1級(Statistical Test Pre-1st grade)
## 22章 例2
### 回答
### 回答

- 用語
    - 寄与率：主成分全体に対する割合$\frac{\lambda_i}{\sum_i^n \lambda_i}$
    - 主成分得点：i番目の実数（or標準化した数）にそれぞれの固有ベクトルを掛けて足したもの
        
        $z_{ik} = \sum^p_{j=1} x_{ji} \cdot \phi_{jk}$
        
        $z_{ik}$: 第k主成分のi番目の得点（主成分得点）
        
        $x_{ij}$: j変数のi番目の標準化データ（標準化前の場合もある）
        
        $\phi_{jk}$: j変数に対する第　　k主成分の固有ベクトル
        
    - 主成分負荷量：もとの変数と主成分の相関係数
        
        $r_{y_j, x_k} = \frac{Cov[x_k, y_j]}{\sqrt{V[y_j] s_P{k,k}}} = \frac{\lambda_ju_{k,j}} {\sqrt{s_{k,k}}}$
        
- (1)
    
    $\frac{20.2+19.4}{20.2+19.4+0.85+0.18} = \frac{39.6}{40.63} = 0.974$
    
    97%以上説明できているので問題ない
    
- (2)
    
    $\frac{\sqrt{\lambda} \cdot u_i(固有ベクトル)}{\sqrt{s_{k,k}(その列の分散)}}　= \frac{\sqrt{19.4} \cdot 0.564}{\sqrt{9.1}} = 0.823$