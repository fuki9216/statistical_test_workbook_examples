## 統計検定準1級(Statistical Test Pre-1st grade)
## 5章 例題3
### 回答
- (1)
    
    1,0なのでXの二乗もXと等しい
    1の期待値を計算すれば良い
    確率は変わらないので
    
    $$
    \frac{3}{9}\cdot 1+ \frac{6}{9}\cdot 0=\frac{1}{3}
    $$
    
- (2)
    
    どちらも1になるパターンを計算すれば良い
    
    $$
    E[X_i X_j] = 1 \cdot \frac{3}{9} \cdot \frac{2}{8} + 0 \cdot (1- \frac{3}{9} \cdot \frac{2}{8})\\
    = \frac{1}{12}
    $$
    
- (3)
    
    $$
    V[\bar{X}] \\
    = V\big[
    \frac{1}{4}(
    X_1 + X_2 + X_3 + X_4
    )\big]+Cov[X_1, X_2]+...+Cov[X_3, X_4]
    
    $$
    
    $Cov[X_i, X_j]$ ：${}_4P_{2} = \frac{n!}{n-r} = \frac{4!}{4-2}=12$ 通り存在する
    
    $E[X_i^2]$ ：(1)より、また $E[X_i]$ も同様なので
    
    $$
    V[X_i] = E[X_i^2] - (E[X_i])^2\\
    = 1/3 - (1/3)^2\\
    = 2/9
    $$
    
    $Cov[X_i, X_j]= E[X_i X_j]-E[X_i]E[X_j] = 1/12 - (1/3)^2=-1/36$ 
    
    $$
    V[\bar{X}]\\
     = (\frac{1}{4})^2+\sum_{i-1}^4 V[X_i] +Cov[X_1, X_2]+...+Cov[X_3, X_4]\\
    = \frac{1}{16}( 4\cdot \frac{2}{9}+ 12\cdot -\frac{1}{36})\\
    = \frac{1}{16}(\frac{5}{9})\\
    = \frac{5}{144}
    $$