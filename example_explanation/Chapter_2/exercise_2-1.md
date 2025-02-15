## 統計検定準1級(Statistical Test Pre-1st grade)
## 2章 例題2-1
### 参考

https://note.com/ebikazuki/n/n0ace45d1cf6a#79c6f57c-74c8-4be1-8213-b7f34d863fad

### 回答

1. 基準化定数 $c$
    
    $$
    \int^1_0 \int^1_0 c(x+y) dx dy = 1\\
    となるように計算する
    $$
    
    $$
    \int^1_0 [c(\frac{1}{2}x^2+y)]^1_0 dy\\
    = \int^1_0 c(\frac{1}{2}+y) dy\\
    = [c(\frac{1}{2} + \frac{1}{2}y^2)]^1_0\\
    = c(\frac{1}{2} + \frac{1}{2})\\
    = c \cdot 1
    $$
    
    上記が1と同じになればよいので $c$ は1となる
    
2. 周辺密度関数
    
    $y$ の範囲0〜1で積分すれば良いので、
    
    $$
    f_X(x) = \int^1_0(x+y)dy = x + \frac{1}{2}
    $$
    
3. 条件付き確率密度関数
    
    条件付き確率密度関数は以下
    
    $$
    f_{Y|X}(y|x) = \frac{f(x,y)}{f_X(x)}
    $$
    
    より
    
    $$
    f_{Y|X}(y|x) = \frac{x+y}{x + \frac{1}{2}}\\
    
    $$