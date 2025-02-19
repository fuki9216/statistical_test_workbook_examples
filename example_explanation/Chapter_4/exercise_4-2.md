## 統計検定準1級(Statistical Test Pre-1st grade)
## 4章 例題2
### 参考
https://qiita.com/tarantula426/items/8b8e9bff11aca418e01d#2%E5%A4%89%E6%95%B0%E3%81%AE%E7%A2%BA%E7%8E%87%E5%AF%86%E5%BA%A6%E9%96%A2%E6%95%B0%E3%81%AE%E5%A4%89%E6%95%B0%E5%A4%89%E6%8F%9B

### 回答

確率変数の線形結合の分布

$Z=aX+bY, W= Y$ とする

この場合の逆変換は以下となる

$X = \frac{Z}{a} - bW$

$Y=W$ 

ヤコビアンは

$$

J = \begin{bmatrix}
\frac{\partial Z}{\partial X} & \frac{\partial Z}{\partial Y} \\
\frac{\partial W}{\partial X} & \frac{\partial W}{\partial Y}
\end{bmatrix}
= \begin{bmatrix}
a & b \\
0 & 1
\end{bmatrix}\\

$$

これにより

$$
= \begin{bmatrix}
1 & 1 \\
0 & 1
\end{bmatrix} =1
$$

逆関数の $X = Z - W , Y = W$ を代入する

$$
\frac{f(x,y)}{|J(x,y)|}= \frac{f(x)f(y)}{|J(x,y)|}\\
= \frac{\lambda e^{-\lambda x} \cdot \lambda e^{-\lambda y} }{1}\\
= \lambda e^{-\lambda (z-w)} \cdot \lambda e^{-\lambda w}\\
= \lambda^2 e^{-\lambda z}
$$

こちらを $W$ で積分すると $f(Z)$ が求められる

$$
\int^Z_0\lambda^2 e^{-\lambda z}dw\\

$$

$w$ がないので外に出す

$$
\lambda^2 e^{-\lambda z}\int^Z_0 dw
$$

$\int^Z_0 dw$ は定積分の長さになるので

$$
\lambda^2 e^{-\lambda z}\cdot z\\
=\lambda^2 z e^{-\lambda z}
$$