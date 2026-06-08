# オンデマンド教材 模範解答

## 第１問

(1) 1から始まる奇数の列は $1,3,5,\ldots,2n-1$であるから、
$$
\sum_{i=1}^{n}(2i-1)
$$
と表せる。

(2) 
* $n=3$ のとき、$1+3+5=9$
* $n=5$ のとき、$1+3+5+7+9=25$

したがって、$9=3^2,\qquad 25=5^2$となる。よって、1から始まる奇数を $n$ 個足すと $n^2$ になると予想できる。

(3) 等差数列の和の公式 $S=\frac{n(a+l)}{2}$を用いる。初項 $a=1$、末項 $l=2n-1$ より、
$$
S= \frac{n\{1+(2n-1)\}}{2}=\frac{n(2n)}{2}=n^2
$$
したがって、$\boxed{\sum_{i=1}^{n}(2i-1)=n^2}$

## 第２問

(1) $f(x)$の式と$g(x)$の式を掛け算すると

$$
h(x)=4^{x+3}\times16^x
$$

$16^x$は$(4^2)^x$であること、および底が等しい指数の掛け算は指数の足し算であることを使って、
$$
4^{x+3}\times16^x=4^{x+3}\times(4^2)^x=4^{x+3}\times4^{2x}=4^{3x+3}
$$
したがって、$\boxed{h(x)=4^{3x+3}}$。

(2) 
底の変換公式 $\log_a b=\frac{\log b}{\log a}$を用いる。ここでは、揃える底を2と設定して、底の変換公式を用いると

$$
{\footnotesize
\begin{align}
\log_2 F \times \log_F D \times \log_D S \times \log_S(FDS) &= \frac{\log_2 F}{\log_2 2}\times\frac{\log_2 D}{\log_2 F} 
\times \frac{\log_2 S}{\log_2 D} \times \frac{\log_2(FDS)}{\log_2 S}\\
&=\frac{\log(FDS_2)}{\log_2 2} \\
&=\log_2(FDS)
\end{align}
}
$$

したがって、$\boxed{\log_2(FDS)}$である。

$F=2,\quad D=4,\quad S=\frac1{16}$を代入すると、

$$
FDS = 2\times4\times\frac{1}{16} =\frac{1}{2}
$$

したがって、

$$
\log_2(FDS)
=
\log_2\left(\frac{1}{2}\right)
=
-1
$$

よって、$\boxed{-1}$。

## 第３問

$$
h(x)=f(g(x))=\log_3(27^x)27=3^3
$$

より、

$$
h(x)=\log_3(3^{3x})=3x
$$

したがって、$\boxed{h(x)=3x}$。

## 第４問

(1) 平均変化率は $\frac{f(4+h)-f(4)}{h}$ である。
$f(x)=\sqrt{x}$ より、

$$
f(4+h)=\sqrt{4+h},
\qquad
f(4)=2
$$

したがって、$\boxed{\frac{\sqrt{4+h}-2}{h}}$。

(2)

$$
\begin{align}
\frac{\sqrt{4+h}-2}{h} \times \frac{\sqrt{4+h}+2}{\sqrt{4+h}+2}
&= \frac{(4+h)-4}{h(\sqrt{4+h}+2)} \\
&= \frac{h}{h(\sqrt{4+h}+2)} \\
&= \frac1{\sqrt{4+h}+2}
\end{align}
$$

したがって、

$$
f'(4) = \lim_{h\to0}\frac1{\sqrt{4+h}+2} = \frac{1}{2+2}= 
\frac{1}{4}
$$

よって、$\boxed{f'(4)=\frac{1}{4}}$ である。

一方、$f(x)=x^{1/2}$より、

$$
f'(x) = \frac12x^{-1/2}
$$

である。$x=4$を代入すると、

$$
\begin{align}
f'(4) &= \frac{1}{2}\times 4^{-1/2} \\
& = \frac{1}{2}\times\frac{1}{\sqrt{4}} \\
& = \frac{1}{2}\times\frac{1}{2} = \frac{1}{4}
\end{align}
$$

となり、先ほど求めた値と一致する。

## 第５問

(1) $f(x)=\log x$ より、$f(1)=\log1=0$。また、

$$
f'(x)=\frac1x
$$

なので、

$$
f'(1)=1
$$

である。したがって、$x=1$における一次近似式は

$$
f(x) \simeq f(1)+f'(1)(x-1) = 0+1(x-1) = x-1
$$
ただし、$\simeq$は「近似的に等しい」を表す。よって、$\boxed{\log x\simeq x-1}\qquad(x\approx1)$ である。

(2) 一次近似式を用いると、$f(1.01)\approx 1.01-1=0.01$。したがって、

$$
\boxed{f(1.01)\approx0.01}
$$

である。

Excelで`=LN(1.01)`を入力すると、

$$
f(1.01)
=
\log(1.01)
\approx
0.00995033
$$

が得られる。0.01と0.00995033は非常に近い値である。したがって、

$$
\log x\simeq x-1
$$

という一次近似式が x=1 の近くでよく成り立つことが確認できる。
