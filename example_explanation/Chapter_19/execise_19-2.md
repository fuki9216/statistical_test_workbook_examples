## 統計検定準1級(Statistical Test Pre-1st grade)
## 19章 例題2
### 回答

生存関数： $S(t)=P(T>t)$ で表し、時間 $t$ までにイベントが発生せず生存している確率

確率密度関数： $S(t)$ を微分したもの

ハザード関数： $h(t) = \frac{f(t)}{S(t)}$ で表し、$t$ 時点までイベントが起こらなかったとき，$t$ 時点以降でイベントが起こる瞬間的な確率

確率密度関数から生存関数を求める

$$
S(t) = P(T>t) = \int^{\infty}_{t} f(t) dt\\
= \int^{\infty}_t\lambda e^{-\lambda t} dt\\
= [\lambda \cdot - \frac{1}{\lambda } e^{ - \lambda t}]^{\infty}_t\\
= lim_{t→\infty}(- e^{-\lambda t} ) + e^{-\lambda t}\\
= lim_{t→\infty}(- \frac{1}{e^{\lambda t}} ) + e^{-\lambda t}\\
= 0 + e^{-\lambda t}
$$

$e$の積分公式：$\int e^{ax} \, dx = \frac{1}{a} e^{ax}$ 

$$
h(t) = \lim_{\Delta t \to 0} \frac{P(t \leq T < t + \Delta t \mid T \geq t)}{\Delta t}  = \frac{S'(t)}{S(t)}\\
= \frac{\lambda e^{-\lambda t}}{e^{-\lambda t}}\\
= \lambda
$$