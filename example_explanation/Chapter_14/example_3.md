## 統計検定準1級(Statistical Test Pre-1st grade)
## 14章 例3
### 回答

A→B、B→C以外はその場に留まっていることに注意する

この場合の確率は

$$
(1-\theta)^{25}\cdot \theta^5 \cdot (0.9-\theta)^{49} \cdot \theta^{1} \cdot 0.9^{50}
$$

対数尤度にして$\theta$に依存しない部分を省くと

$$
log\ L(\theta) = 25log\ (1-\theta)+5 log\ \theta + 49 log\ (0.9-\theta) + log\ \theta\\

$$

上記を微分した結果を0とすると

$$
-\frac{25}{1-\theta}+ \frac{5}{\theta}- \frac{49}{0.9 - \theta} + \frac{1}{\theta} = 0\\
-\frac{25}{1-\theta}+ \frac{6}{\theta}- \frac{49}{0.9 - \theta} = 0\\
\frac{-25(0.9-\theta)\theta - 49(1-\theta)\theta + 6(1-\theta)(0.9-\theta)}{(1-\theta)(0.9-\theta)\theta} = 0\\
80\theta^2 - 82.9\theta + 5.4 = 0

$$

解の公式 $\theta = \frac{-b \pm \sqrt{b^2- 4ac}}{2a}$ より

$$
 \frac{- (-82.9) \pm \sqrt{(-82.9)^2 - 4\cdot 80\cdot 5.4}}{2\cdot 80}\\
= \frac{-(-82.9) \pm \sqrt{6872.41 - 1728}}{160}\\
= \frac{82.9 \pm 71.72}{160}\\

$$

$\theta= 0.966, 0.0069$

$\theta <0.5$より約0.07となる