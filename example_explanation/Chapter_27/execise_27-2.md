## 統計検定準1級(Statistical Test Pre-1st grade)
## 27章 例題2
### 用語
- 移動平均過程（MA過程）
    
    1次の式：$Y_t = \mu + U_t + \theta_1 U_{t-1}$
    
    $q$次の移動平均過程
    
    分散 $\gamma_0 = (1+\theta_1^2+ ...+\theta_q^2 )\sigma^2$
    
    自己共分散：$(\theta_h + \theta_1 \theta_{h=1},...+\theta_{q-h}\theta_q)\sigma^2$
    
- 自己回帰移動平均過程（ARMA過程）
    
    階差($\Delta Y=Y_t - Y_{y-1}$)を用いた自己回帰移動平均過程は「自己回帰和分移動平均過程（ARIMA）」
    
- ディッキーフラー検定(AR過程は拡張ディッキーフラー検定)
    
    自己回帰過程において階差を取る必要があるのかを検定する
    
    帰無仮説：$\phi = 1$
    
    対立仮説：$|\phi| < 1$
    
- 次数の選択
    
    
    | 自己相関係数
    （AR過程でゆっくり減衰） | 編自己相関係数
    （MA過程でゆっくり減衰） | 選択するモデル |
    | --- | --- | --- |
    | 2次以降0 | ゆっくり減衰 | MA(1) |
    | 3次以降0 | ゆっくり減衰 | MA(2) |
    | ゆっくり減衰 | 2次以降0 | AR(1) |
    | ゆっくり減衰 | 3次以降0 | AR(2) |
    | ゆっくり減衰 | ゆっくり減衰 | ARMA(1,1 |

### 回答

自己共分散

- ラグ0の場合
    
    $$
    Cov(Y_t, Y_t) = V[Y_t]\\
    = E[Y_t^2] - (E[Y_t])^2
    $$
    $E[Y_t]$ の計算
    $$
    E[Y_t] = E[U_t + \theta_1 U_{t-1} + \theta_2 U_{t-2}]\\
    = E[U_t]+ E[\theta_1 U_{t-1}] +E[ \theta_2 U_{t-2}]\\
    = 0+0+0
    $$
    
    $U_t$はホワイトノイズなので期待値0
    
    $$
    Cov(Y_t, Y_t) = E[Y_t^2]\\
    =E[(U_t + \theta_1 U_{t-1} + \theta_2 U_{t-2})^2]\\
    = E[U_t^2 + \theta_1^2 U_{t-1}^2 +\theta_2^2 U_{t-2}^2 + 2\theta_1 U_t U_{t-1} + 2\theta_2U_t U_{t-2} + 2\theta_1 U_{t-1} U_{t-2}]
    $$
    
    ホワイトノイズは以下の性質がある
    
    $E[U_t] = 0$
    
    $E[U_t^2] = \sigma^2$
    
    $E[U_t U_{t-k}]=0$
    
    上記に適応すると
    
    $$
    \sigma^2 + \theta_1^2 \sigma^2 + \theta_2^2 \sigma^2\\
    = \sigma^2(1+\theta_1^2 + \theta_2^2)
    $$
    
- ラグ1の場合
    
    $$
    \gamma(1) = Cov(Y_t, Y_{t-1})\\
    = E[(Y_t - E[Y_t])(Y_{t-1} - E[Y_{t-1}])]
    $$
    
    $U_t$はホワイトノイズのため、$E[Y_t]=0$となるので
    
    $$
     E[Y_t\ Y_{t-1}]
    $$
    
    $Y_t = U_t + \theta_1 U_{t-1} + \theta_2 U_{t-2}$
    
    $Y_{t-1} = U_{t-1} + \theta_1 U_{t-2} + \theta_2 U_{t-3}$
    
    $$
    Y_t Y_{t-1}\\
     = (U_t + \theta_1 U_{t-1} + \theta_2 U_{t-2})(U_{t-1} + \theta_1 U_{t-2} + \theta_2 U_{t-3})\\
    = U_t U_{t-1} + \theta_1 U_t U_{t-2} + \theta_2 U_t U_{t-3}\\
     + \theta_1 U_{t-1}^2 + \theta_1^2 U_{t-1} U_{t-2} + \theta_1 \theta_2 U_{t-1} U_{t-3}\\
    + \theta_2 U_{t-2} U_{t-1} + \theta_1 \theta_2 U_{t-2}^2 + \theta_2^2 U_{t-2} U_{t-3}
    $$
    
    ホワイトノイズの性質
    
    $E[U_t] = 0$
    
    $E[U_t^2] = \sigma^2$
    
    $E[U_t\ U_{t-k}]= 0$
    
    $$
    \theta_1 E[U^2_{t-1}] + \theta_1 \theta_2 E[U^2_{t-2}]\\
    = \theta_1 \sigma^2 + \theta_1 \theta_2 \sigma^2\\
    = \sigma^2 (\theta_1 + \theta_1 \theta_2)
    $$
    
- ラグ2の場合
    
    ラグ1と同様に$E[Y_t\ Y_{t-2}]$
    
    $$
    E[
    (U_t + \theta_1 U_{t-1} + \theta_2 U_{t-2})
    (U_{t-2} + \theta_1 U_{t-3} + \theta_2 U_{t-4})
    ]\\
    E[
    U_t U_{t-2} + \theta_1 U_t U_{t-3} + \theta_2 U_t U_{t-4}\\
    \theta_1 U_{t-1}U_{t-2}+ \theta_1^2 U_{t-1}U_{t-3} + \theta_1 \theta_2 U_{t-1}U_{t-4}\\
    \theta_2 U_{t-2}^2 +\theta_1 \theta_2 U_{t-2} U_{t-3} + \theta^2 U_{t-2}U_{t-4}
    ]
    $$
    
    ホワイトノイズの性質
    
    $E[U_t] = 0$
    
    $E[U_t^2] = \sigma^2$
    
    $E[U_t\ U_{t-k}]= 0$
    
    より
    
    $$
    \theta_2 \sigma^2
    $$
    

ラグ3以降は0