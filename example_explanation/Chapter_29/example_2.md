## 統計検定準1級(Statistical Test Pre-1st grade)
## 29章 例2
### 回答

| x | y |
| --- | --- |
| 35 | 40 |
| 37 | 38 |
| 40 | 48 |
| 45 | 41 |
| 47 | 60 |
| 54 | 46 |
| 57 | 57 |
| 60 |  |
| 62 |  |
| 63 |  |

$x$ の全てを利用した統計量

$\bar{x} = 50$

$\bar{\sigma_x^2} = 100.6$

欠損が無い7組のデータのそれぞれの統計量は

$\bar{x} = 45$

$\bar{s_x^2} = 59.71$

$\bar{y} = 47.14$

$\bar{s_y^2} = 62.41$

$r = \frac{39.14}{\sqrt{59.71 \cdot 47.14}}=0.7377$

回帰パラメータの推定値

誤差分散 $\hat{t} = s_Y^2 - \frac{(s_{xy})^2}{s_x^2} = 62.41 - \frac{(39.14)^2}{59.71} = 36.75$

$\hat{a} = \bar{y} - b \bar{x} = 47.14 - 0.655 \cdot 45 = 17.655$

$\hat{\beta} = \frac{s_{xy}^2}{s_x^2} =\frac{39.14}{59.71}= 0.655$

上記より$X$の周辺分布以外のパラメータの最尤推定値は以下のようになる

$\hat{\mu_Y} = \hat{\alpha} + \hat{\beta} \hat{x} = 17.65 + 0.655 \cdot 50 = 50.65$ 

$\hat{\sigma}^2_Y = \hat{t}^2 + \hat{\beta}^2 \cdot \hat{\sigma^2}_X = 36.75 + 0.655 \cdot 100.6 = 80.57$ 

$\hat{\sigma}_{XY} = \hat{\beta} \cdot \hat{\sigma^2}_X =0.655 \cdot 100.6  = 65.94$ 

$\hat{p} = \frac{\hat{\sigma}_{XY}}{\sqrt{\hat{\sigma_X}\hat{\sigma_Y}}}= \frac{65.94}{\sqrt{100.6\cdot 80.57}} = 0.74$