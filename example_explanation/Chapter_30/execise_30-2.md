## 統計検定準1級(Statistical Test Pre-1st grade)
## 30　章 例題2
### 回答

最大尤度 $L = \big(\frac{2\pi S_e}{n} \big)^{-\frac{n}{2}} e^{-\frac{n}{2}}$

AIC：$-2 log L + 2k$

BIC：$-2log L + k\ log\ n$

説明変数無しの場合のAIC

$$
log\ L = -\frac{20}{2} log \big(\frac{2 \pi S_e}{20} \big) - \frac{20}{2}\\
= -10 (log\ 2\pi + log\ S_e - log\ 20)- 10\\
= -10(1.838 + 10.881 - 2.996) - 10\\
= -10 \cdot 9.723 -10\\
=-107.23
$$

$$
-2log\ L\ + 2k\\
=-2 \cdot -107.23 + 2\cdot 2\\
= 214.46 + 4 = 218.46
$$

説明変数無しの場合のBIC

$$
-2 log L + k\ log\ n\\
= -2 \cdot -107.23 + 2 log 20\\
= 214.46 + 2\cdot 2.996\\
= 220.452
$$