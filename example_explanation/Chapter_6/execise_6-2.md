## 統計検定準1級(Statistical Test Pre-1st grade)
## 6章 例題2

### 回答

- (1)
    
    $$
    V[X+Y] = V[X] + V[Y] + 2Cov[X,Y]\\
    
    相関係数=\frac{Cov[X,Y]}{\sqrt{V[X]} \sqrt{V[Y]}}
    $$
    
    より
    
    $$
    150^2 = 80^2 + 90^2 +2Cov[Listening,Reading]\\
    Cov[Listening,Reading]= (150^2-80^2-90^2)/2 =4000
    $$
    
    $$
    r = \frac{4000}{80 \cdot 90}\\
    = 0.5555...
    $$
    
- (2)
    
    $$
    2変量正規分布の条件付き期待値\\
    = E[Y] + r[X,Y]\cdot \frac{\sqrt{V[Y]}}{\sqrt{V[X]}}(x - E[X])\\
    
    250 + 0.556 \cdot \frac{90}{80}(335- 305)= 268.8
    $$