## 統計検定準1級(Statistical Test Pre-1st grade)
## 19章 例題1
### 回答

- (1)
    
    トービットモデルの尤度関数
    
    $$
    L(\beta, \sigma) = \prod_{i:y_i>L} \frac{1}{\sigma} \phi (\frac{y_i - x_i^T \beta}{\sigma}) \prod_{i:y_i<L} \Phi (\frac{L- x_i^T \beta}{\sigma}) 
    $$
    
    $\prod_{i:y_i>L} \frac{1}{\sigma} \phi (\frac{y_i - x_i^T \beta}{\sigma})$ ：検閲されたデータ$(y_i < L)$の場合の確率
    
    $\phi$：正規分布の確率密度
    
    $\prod_{i:y_i<L} \Phi (\frac{L- x_i^T \beta}{\sigma})$ ：検閲されてないデータ$(y_i >L)$の場合の確率密度
    
    $\Phi$：正規分布の累積分布関数
    
    より今回は積雪量は0を下回ることは無いので、0での左打ち切り
    
    $$
    \prod_{i:y_i>0}\frac{1}{\sigma} \phi (\frac{y_i - (\beta_0 + \beta_1 x_{i1} + \beta_2 x_{i2})}{\sigma}) \cdot \prod_{i:y_i<0}\Phi (\frac{0- (\beta_0 + \beta_1 x_{i1} + \beta_2 x_{i2})}{\sigma})
    $$
    
- (2)
    
    AIC：小さいほうが良いモデル
    
    $$
    AIC = -2 \cdot 最大対数尤度 + 2パラメータ数
    $$
    
    パラメータは$切片、誤差項、説明変数の数$より、
    
    計算すると日照時間+平均気温が良いモデル