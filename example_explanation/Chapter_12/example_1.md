## 統計検定準1級(Statistical Test Pre-1st grade)
## 12章 例1
### 回答

母比率の検定

- 漸近正規生を用いた検定
    
    二項分布の比率の検定において、漸近正規性を用いて棄却限界域を決めて検定を行う
    
    $\theta = \theta_0$とする帰無仮説の元で$n→\infty$として
    
    $$
    \frac{\sqrt{n}(\hat{\theta} - \theta_0)}{\sqrt{\theta_0(1- \theta_0)}}
    $$
    
    が標準正規分布に収束する
    
    ※$\theta_0(1- \theta_0)$：分散
    
    上記より$Z$値は
    
    $$
    \frac{\sqrt{n}(\hat{\theta} - \theta_0)}{\sqrt{\theta_0(1- \theta_0)}}\\
    = \frac{\sqrt{30}(\frac{12}{30} -  0.5)}{\sqrt{0.5(1- 0.5)}}\\
    = \frac{0.5477}{0.5}\\
    = -1.0954..
    $$
    
    となるので、上側2.5%の1.96より小さいため棄却されない
    
- 尤度比検定の場合
    
    尤度比検定の場合は
    
    $$
    2\cdot n \big( \hat{\theta} \cdot log \frac{\hat{\theta}}{\theta_0} + (1- \hat{\theta})\ log\ \frac{1- \hat{\theta}}{1-\theta_0}\big) \geq X^2_\alpha(1)
    $$
    
    のようにカイ二乗分布を用いて検定する
    
    $$
    2\cdot 30(0.4\ log\ \frac{0.4}{0.5} + (1- 0.4)\ log\ \frac{1-0.4}{1-0.5})\\
    
    $$
    
    計算すると1.21となる
    
    自由度は「 $観測値の数 - 指定されたパラメータ数$ 」より1
    
    上側5%は3.84なので棄却できない