### 回答

- (1)
    
    $V[x] = E[x^2] - (E[x])^2$ より
    
    $$
    E[x^2]= \int^1_0 1-u^2 dx \\
    = \int^1_0 1 - \int^1_0 u^2\\
    =[u]^1_0 - [1/3u^3 ]^1_0\\
    = 1- 1/3 = 2/3
    $$
    
    $$
    V[\sqrt{1-u^2}]= 2/3 - (\pi/4)^2\\
    = 0.666... - 0.6262..\\
    = 0.05..
    $$
    
    $\hat{\pi} = 4\cdot \frac{1}{n} \sum^n_{i=1} \sqrt{1-U^2}$ より標準偏差 $SD[\hat{\pi}]$ は
    
    $$
    V[\hat{\pi}] = V[4\cdot \frac{1}{n} \sum^n_{i=1} \sqrt{1-U^2}]\\
    = 4^2 \frac{1}{n^2}\sum^n_{i=1} V[\sqrt{1-U^2}]\\
    = 4^2 \frac{1}{n}\cdot 0.05\\
    
    $$
    
    $$
    SD[\hat{\pi}] = \sqrt{4^2\cdot \frac{1}{n} 0.05} \\
    = \frac{4\sqrt{0.05}}{\sqrt{n}}
    $$
    
    こちらが0.01の場合を考える
    
    $$
    \frac{4\sqrt{0.05}}{\sqrt{n}} =0.01\\
    \frac{16\cdot 0.05}{n} =0.0001\\
    n = 8000
    $$
    

- (2)
    
    $V[\hat{\pi}] = V[4\cdot \frac{1}{4}\sum^{n}_{i=1} \sqrt{1-U^2_i} - (1/2 - U_i)]$
    
    $$
    V[\hat{\pi}] = V[4\cdot \frac{1}{n}\sum^{n}_{i=1} \sqrt{1-U^2_i} - (1/2 - U_i)]\\
    \frac{4^2}{n^2}\sum^{n}_{i=1} V[\sqrt{1-U^2_i} - (1/2 - U_i)]\\
    $$
    

連携分布の分散の公式より

$$
V[x] = \int^b_a (x-m)^2 f(x) dx\\
を用いて\\
V[\sqrt{1-U^2_i} - (1/2 - U_i)]\\
= \int^1_0\big((\sqrt{1-U^2_i}-(1/2-U_i)) - E[\sqrt{1-U^2_i}-(1/2-U_i)] \big)^2 \cdot \frac{1}{1-0}dx\\
= \int^1_0\big((\sqrt{1-U^2_i}-(1/2-U_i)) - E[\sqrt{1-U^2_i}]+E[(1/2-U_i)] \big)^2 \cdot \frac{1}{1-0}dx\\
$$

$E[\sqrt{1-U^2_i}]$ ：(1)より$4/\pi$

$E[1/2 - U_i]$ ：問題より0

こちらを用いて

$$
= \int^1_0\big(\sqrt{1-U^2_i} + u -\frac{1}{2}  - \frac{4}{\pi}\big)^2\\
問題より\\
= 0.0144

$$

$$
V[\hat{\pi}] = \frac{4^2}{n^2}\sum^n_{i=1}  0.0144\\
= \frac{16}{n} 0.0144
$$

標準偏差が0.01になるには

$$
\sqrt{\frac{16}{n} 0.0144} =0.01\\
\frac{16}{n} 0.0144 = 0.0001\\
n = 16\cdot 0.0144 \cdot 10000\\
= 2304
$$