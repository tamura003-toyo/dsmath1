# 偏微分と最適化

## 2変数の関数の変化率を求める

$$
S(a, b) = 14a^2 + 12ab + 3b^2 -36a -16b +24
$$

## 最小二乗法

| x | y |
|---|---|
| 1 | 2 |
| 2 | 2 |
| 3 | 3 |

$$
y = ax + b
$$

$$
e = \sum_{i=1}^3 (y_i - (ax_i + b))^2
$$

### 誤差の最小化

$$
S(a,b)
=(2-(a+b))^2
+(2-(2a+b))^2
+(4-(3a+b))^2
$$

### 考え方


```{note} ✏️ 解答
:class: dropdown
:open: false
:icon: false
関数$S$の$a$に関する偏微分を計算する。
$$
\begin{aligned}
\frac{\partial S(a,b)}{\partial a} & =  2(2-a-b)\times(-1)\\
& +2(2-2a-b)\times(-2) \\
& +2(4-3a-b)\times (-3) \\
& = (-4+2a+2b) + (-8+8a+4b) + (-24+18a+6b) \\
& = -36 + 28a + 12b 
\end{aligned}
$$

関数$S$の$b$に関する偏微分を計算する。

$$
\begin{aligned}
\frac{\partial S(a,b)}{\partial b} & =  2(2-a-b)\times(-1)\\
& +2(2-2a-b)\times(-1) \\
& +2(4-3a-b)\times (-1) \\
& = (-4+2a+2b) + (-4+4a+2b) + (-8+6a+2b) \\
& = -16 + 12a + 6b 
\end{aligned}
$$

極値条件は、次のように書くことができる。

$$
\begin{cases}
\frac{\partial S(a,b)}{\partial a} &=& 0 \\
\frac{\partial S(a,b)}{\partial b} &=& 0
\end{cases}
$$

偏微分した式を使って表記し直すと、

$$
\begin{cases}
-36 + 28a + 12b  = 0 \\
-16 + 12a + 6b  = 0
\end{cases}
$$

結局、未知数が$a,b$の二元連立方程式を解くことに帰着できる。ここでは消去法を用いて$b$を消去する解法を使おう。

第2式の両辺を2倍して第1式との差をとると、
$$
-4 + 4a = 0\iff a = 1
$$
よって、$b$の値は
$$
-16 + 12\times 1 +  6b = 0 \iff -4 + 6b = 0 \iff b = \frac{2}{3}
$$
以上より、3つの点の中を貫く直線の中で、最も誤差が小さくなる直線は
$$
y = x + \frac{2}{3}
$$
と求まった。
```
### これ
```{image} images/10_ols1.png
:alt: Grapes on a vineyard
:width: 70%
:align: center
```

[損失関数の概要と、最適化した点の位置](./_static/10_plotly_ols_surface.html)


