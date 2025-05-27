- [スカラービーム](#スカラービーム)
- [楕円率](#楕円率)
- [射影演算子](#射影演算子)
- [スカラービームの表現](#スカラービームの表現)
- [パウリ行列展開](#パウリ行列展開)
- [ストークスパラメーター](#ストークスパラメーター)
- [ポアンカレ球](#ポアンカレ球)
- [1/2波長板](#12波長板)
- [1/4波長板](#14波長板)
- [直線偏光子](#直線偏光子)

## スカラービーム

ベクトルビームについて考える前に直線偏光,楕円偏光,円偏光などのスカラービームについて考えます.楕円偏光は直線偏光と円偏光の中間に位置するような偏光状態でその名の通り振動の軌跡が楕円になっています.以下ではこれらの分類,もしくは各偏光状態がどのようなパラメーターを持っているのかを考えます.

## 楕円率

上に挙げた3つの偏光状態はまとめて楕円偏光と呼ぶことができます.つまり直線偏光と円偏光を楕円偏光の特殊な形と考えるということです.

その偏光状態がどれだけ"楕円らしいか"を表す指標に **楕円率** というものがあります.これは単に数学でやるような幾何学的なものです.これについて説明します.

電場のx,y成分を

$$
\begin{aligned}
E _ {x} &= E _ {x0} \cos{(kz-\omega t)} \newline
E _ {y} &= E _ {y0} \cos{(kz-\omega t+\epsilon)}
\end{aligned}
$$

と表します.繰り返しますが偏光を考えるうえで重要なのは振幅 $E _ {x0},E _ {y0}$ の比と位相差 $\varepsilon$ のみです.よってこれらだけのパラメーターでこの偏光状態を表したいです.(zやtの変数を消したい.)まずy成分は

$$
\frac{E _ {y}}{E _ {y0}} = \cos{(kz-\omega t)}\cos{\varepsilon}-\sin{(kz-\omega t)}\sin{\varepsilon}
$$

のように書けます.ここにx成分を代入すると

$$
\frac{E _ {y}}{E _ {y0}} = \frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}-\sin{(kz-\omega t)}\sin{\varepsilon}
$$

となります.またx成分をsinで表すと

$$
\begin{aligned}
E _ {x}&=E _ {x0} \sqrt{1-\sin^2{(kz-\omega t)}} \newline
\sin{(kz-\omega t)}&=\sqrt{1-\frac{E _ x}{E _ {x0}}^2}
\end{aligned}
$$

となるので結局

$$
\frac{E _ {y}}{E _ {y0}} = \frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}-\sqrt{1-\frac{E _ x}{E _ {x0}}^2}\sin{\varepsilon}
$$

となりz,tを失くすことができました.移項して両辺を二乗すると

$$
\Bigl(\frac{E _ {y}}{E _ {y0}}-\frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}\Bigr)^2=(1-\frac{E _ x}{E _ {x0}})\sin^2{\varepsilon}
$$

$$
\Bigl(\frac{E _ {x}}{E _ {x0}}\Bigr)^2+\Bigl(\frac{E _ {y}}{E _ {y0}}\Bigr)^2-2\frac{E _ {x}E _ y}{E _ {x0}E _ {y0}} \cos{\varepsilon}=\sin^2{\varepsilon}
$$

## 射影演算子

今までの説明では偏光を表すときにジョーンズベクトルの各成分の振幅比と位相差のみが重要と言ってきました.つまりジョーンズベクトルが

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

と書けるとき,

$$
\vert \alpha \vert ^2 + \vert \beta \vert ^2 = 1
$$

としても任意の振幅比も表現できる。

ここで天下り的だが以下のようにジョーンズベクトルから行列を作る。

$$
P = \begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^*
$$

これは**射影演算子**と呼ばれる。

ただしどんな行列も射影演算子となるわけではなく以下の2つを満たす必要がある。(線形写像となる条件？)

$$
\begin{aligned}
-P^2 &= 1 \newline
P^ \dagger &= P
\end{aligned}
$$

計算してみると、確かに

$$
\begin{aligned}
P^2 &= (
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} 
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* ) (
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* ) \newline
&= 
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} (
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^*  
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} )
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* \newline
&= 
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} (
| \alpha | ^2 + | \beta | ^2 )
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* \newline
\therefore P^2 &= P
\end{aligned}
$$

次に

$$
\begin{aligned}
P ^{\dagger}
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* ) ^{\dagger} \newline
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* ) ^{\dagger} \newline
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
^* )^*
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* \newline
\therefore P^{\dagger} 
&=
P
\end{aligned}
$$

## スカラービームの表現

任意のスカラービームは２つの直交基底ベクトルの重ね合わせで表現できる

ジョーンズベクトルを

$$
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
(\alpha, \beta \in C)
$$

と表したときストークスパラメーターという実数値は

$$
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix} =
\begin{bmatrix}
\vert \alpha \vert ^2 - \vert \beta \vert ^2 \newline
2 Re(\alpha \beta ^\ast) \newline
-2 Im(\alpha \beta ^\ast)
\end{bmatrix}
$$

例えばジョーンズベクトルが

$$
\frac{1}{\sqrt{2}}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
=\frac{1}{\sqrt{2}}(\alpha
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+\beta
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
)
$$

のように垂直、水平偏光の重ね合わせでと書けるとする。

これを左右円偏光の重ね合わせで書くと

$$
\frac{1}{2\sqrt{2}} \Bigl ( (\alpha-i\beta)
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
\Bigr ) +
\frac{1}{2\sqrt{2}} \Bigl ( (\alpha+i\beta)
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
\Bigr )
$$

逆に

$$
\alpha _ 2
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+
\beta _ 2
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
$$

と書けるとき

$$
(\alpha _ 2 + \beta _ 2)
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+i(\alpha _ 2 - \beta _ 2)
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
$$

$$
\begin{aligned}
\vec{\psi}
&=
\alpha
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+\beta
\begin{bmatrix}
1 \newline
-i
\end{bmatrix} \newline
&=
(\alpha+\beta)
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+i(\alpha+\beta)
\begin{bmatrix}
0 \newline
1
\end{bmatrix} \newline
&=
\frac{1}{2}(1+i)(\alpha+\beta)
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
+\frac{1}{2}(1-i)(\alpha+\beta)
\begin{bmatrix}
1 \newline
-1
\end{bmatrix}
\end{aligned}
$$

$$
\vec{\psi} = e^{-i\varphi}\cos{\Bigl (\theta+\frac{\pi}{4}\Bigr )}
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+
e^{i\varphi}\sin{\Bigl (\theta+\frac{\pi}{4}\Bigr )}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
$$

## パウリ行列展開

パウリ行列は

$$
\sigma_0 =
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}, \quad
\sigma_1 =
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}, \quad
\sigma_2 =
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}, \quad
\sigma_3 =
\begin{bmatrix}
0 & -i \newline
i & 0
\end{bmatrix}
$$

で表される。

さきほどのジョーンズベクトルから作った行列をパウリ行列の和で表すことを考える。

ここでパウリ行列の性質として、例えば

$$
\begin{aligned}
\sigma _ 2 ^2 &=
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix} \newline
&= 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
\end{aligned}
$$

となり2乗すると単位行列であり、

異なる行列同士の積のTrを考えると、例えば

$$
\begin{aligned}
Tr( \sigma _ 3 \sigma _ 2 ) &= Tr \Bigl (
\begin{bmatrix}
0 & -i \newline
i & 0
\end{bmatrix}
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix} \Bigr ) \newline
&= Tr \Bigl (
\begin{bmatrix}
-i & 0 \newline
0 & i
\end{bmatrix} \Bigr ) \newline
&= 
-i + i \newline
\therefore Tr( \sigma _ 3 \sigma _ 2 ) 
&=
0
\end{aligned}
$$

となり0となる。

これら2つの性質を使うと、以下のようにパウリ行列の和で表したとき、

$$
\begin{aligned}
P &= \frac{1}{2} (
h _ 0 \sigma _ 0 + h _ 1
\sigma _ 1 + h _ 2 \sigma _ 2 + h _ 3 \sigma _ 3 ) \newline
&= \frac {1} {2} \Bigl (
h_0 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+h _ 1
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+h _ 2
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
+h _ 3
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix} 
\Bigr )
\end{aligned}
$$

と仮定すると

先ほどの積の性質を使えば、例えば

$$
\begin{aligned}
\mathrm{Tr}(P \sigma _ 3) &= \frac{1}{2} \Bigl(h_0 \mathrm{Tr}(\sigma _ 0 \sigma _ 3) + h _ 1 \mathrm{Tr}(\sigma _ 1 \sigma _ 3) + h _ 2 \mathrm{Tr}(\sigma _ 2 \sigma _ 3) + h _ 3 \mathrm{Tr}(\sigma _ 3 \sigma _ 3) \Bigr) \newline
&=
h_3 \newline
&=
2 \mathrm{Tr} \Bigl(
\begin{bmatrix}
\mid \alpha \mid ^2 & \alpha \beta ^ \ast \newline
\alpha  \ast* \beta & \mid \beta \mid ^2
\end{bmatrix}
\begin{bmatrix}
0 & -i \newline
 i & 0
\end{bmatrix}
\Bigr) \newline
&=
\mathrm{Tr} \Bigl( 
\begin{bmatrix}
i \alpha \beta^* & -i \mid \alpha \mid ^2 \newline
i \mid \beta \mid ^2 & -i \alpha ^\ast \beta
\end{bmatrix}
\Bigr) \newline
&=
i (\alpha \beta ^ \ast - \alpha ^ \ast \beta) \newline
&=
-2 \mathrm{Im}(\alpha \beta ^ \ast) \newline
\therefore h_3
&=
-2 \mathrm{Im}(\alpha \beta ^ \ast)
\end{aligned}
$$


のように係数が求められる。

他も同じように計算すると結局

$$
\begin{aligned}
P
&=
\frac{1}{2} (
h _ 0 \sigma _ 0 + h _ 1 \sigma _ 1 + h _ 2 \sigma _ 2 + h _ 3 \sigma _ 3 ) \newline
&=
\frac{1}{2} \Bigl (
h_0 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+h_1
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+h_2
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
+h_3
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix}
\Bigr ) \newline
&=
\frac{1}{2} \Bigl (
\bigl (\mid \alpha \mid ^2 + \mid \beta \mid ^2 \bigr )
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+\bigl (\mid \alpha \mid ^2 - \mid \beta \mid ^2 \bigr )
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+2 Re( \alpha \beta ^ \ast)
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
-2 Im( \alpha \beta ^ \ast)
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix}
\Bigr )
\end{aligned}
$$

今は $|\alpha| ^2 + |\beta| ^2 = 1$ を考えているので第一項目の係数は1になるため、以下では $h_1, h_2, h_3$ のみを考える。

この係数をベクトルとしたもの

$$
\begin{aligned}
\boldsymbol{ S }
&= 
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\newline
&=
\begin{bmatrix}
h _ 1 \newline
h _ 2 \newline
h _ 3
\end{bmatrix}
\newline
\therefore \boldsymbol{S}
&= 
\begin{bmatrix}
\mid \alpha \mid ^2 - \mid \beta \mid ^2 \newline
2 Re( \alpha \beta ^ \ast) \newline
-2 Im( \alpha \beta ^ \ast)
\end{bmatrix}
\end{aligned}
$$

となりストークスベクトルを導出できた。

## ストークスパラメーター

次にストークスパラメーターを計算します.

$$
\begin{aligned}
S' _ 1&=(Re(\alpha)\cos{\delta}-Im(\alpha)\sin{\delta})^2+(Re(\alpha)\sin{\delta}+Im(\alpha)\cos{\delta})^2+Re^2(\beta)+Im^2(\beta) \newline
&=Re^2(\alpha)\cos^2{\delta}-2Re(\alpha)Im(\alpha)\sin{\delta}\cos{\delta}+Im^2(\alpha)\sin^2{\delta}+Re^2(\alpha)\sin^2{\delta}+2Re(\alpha)Im(\alpha)\sin{\delta}\cos{\delta}+Im^2(\alpha)\cos^2{\delta}+\vert \beta \vert^2 \newline
&=Re^2(\alpha)+Im^2(\alpha)+\vert \beta \vert^2 \newline
\therefore S' _ 1&=\vert \alpha \vert^2+\vert \beta \vert^2=S _ 1
\end{aligned}
$$

$$
\begin{aligned}
\alpha' \beta'^\ast&=-\bigl(Re(\alpha)\cos{\delta}-Im(\alpha)\sin{\delta}+i(Re(\alpha)\sin{\delta}+Im(\alpha)\cos{\delta})\bigr)(Re(\beta)-iIm(\beta)) \newline
&=Re(\beta)Im(\alpha)\sin{\delta}-Re(\alpha)Re(\beta)\cos{\delta}-Re(\alpha)Im(\beta)\sin{\delta}-Im(\alpha)Im(\beta)\cos{\delta}+i(Re(\alpha)Im(\beta)\cos{\delta}-Re(\alpha)Re(\beta)\sin{\delta}-Im(\alpha)Im(\beta)\sin{\delta}-Re(\beta)Im(\alpha)\cos{\delta})
\end{aligned}
$$

となるが

$$
\alpha \beta^\ast=Re(\alpha)Re(\beta)+Im(\alpha)Im(\beta)+i(Re(\beta)Im(\alpha)-Re(\alpha)Im(\beta))
$$

であるので

$$
\alpha'\beta'^\ast=-Re(\alpha \beta^\ast)\cos{\delta}+Im(\alpha \beta^\ast)\sin{\delta}+i(-Re(\alpha \beta^\ast)\sin{\delta}-Im(\alpha \beta^\ast)\cos{\delta})
$$

となります.よって

$$
\begin{aligned}
S' _ 2&=2Re(\alpha' \beta'^\ast) \newline
&=-2Re(\alpha \beta^\ast)\cos{\delta}+2Im(\alpha \beta^\ast)\sin{\delta} \newline
\therefore S' _ 2 &= -S _ 2\cos{\delta}-S _ 3\sin{\delta}
\end{aligned}
$$

$$
\begin{aligned}
S' _ 3&=-2Im(\alpha' \beta'^\ast) \newline
&=-2Re(\alpha \beta^\ast)\sin{\delta}-2Im(\alpha \beta^\ast)\cos{\delta} \newline
\therefore S' _ 2 &= -S _ 2\sin{\delta}+S _ 3\cos{\delta}
\end{aligned}
$$

$$
\begin{aligned}
\vec{S'} &=
\begin{bmatrix}
S _ 1 \newline
-S _ 2\cos{\delta}-S _ 3\sin{\delta} \newline
-S _ 2\sin{\delta}+S _ 3\cos{\delta}
\end{bmatrix} \newline
\therefore \vec{S'}&=\begin{bmatrix}
1 & 0 & 0 \newline
0 & -\cos{\delta} & -\sin{\delta} \newline
0 & -\sin{\delta} & \cos{\delta}
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

## ポアンカレ球

実は計算すると分かるが先ほど導出したストークスパラメーターは

$$
S^2 _ 1 + S^2 _ 2 + S^2 _ 3 = 1
$$


の関係がある。

これはストークスベクトルが

 $S_1, S_2, S_3$ **を軸とした単位球面上の1点を指している。**

ということを表している。

また、これまで波長板について話してきたが、

**波長板によって光の偏光分布が変わるということはジョーンズベクトルが変わる、つまりストークスベクトルが変わる、つまりポアンカレ球面上で別の座標に移る。**

ということを意味している。

**波長板によってポアンカレ球上の座標がくるくると移動するということ。**

※このように長さを変えない(今は球の表面上で移動する)写像を等長写像という。

水平偏光が $(S_1, S_2, S_3) = (1, 0, 0)$

右回り円偏光が $(S_1, S_2, S_3) = (0, 0, 1)$

など。

## 1/2波長板

ポアンカレ球表面上で1/2波長板の影響によって点がどのように移るかを考えます.
例によってジョーンズベクトルが

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

と書けるとき,このジョーンズベクトルに$\theta$回転させた1/2波長板を作用させると $\alpha=\alpha _ 1+i\alpha _ 2,\beta=\beta _ 1+i\beta _ 2$

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix} &=
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&= \begin{bmatrix}
\alpha \cos{2\theta} + \beta \sin{2\theta} \newline
\alpha \sin{2\theta} - \beta \cos{2\theta}
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\begin{bmatrix}
\alpha _ 1 \cos{2\theta}+\beta _ 1 \sin{2\theta}+i(\alpha _ 2 \cos{2\theta}+\beta _ 2 \sin{2\theta}) \newline
\alpha _ 1 \sin{2\theta}-\beta _ 1 \cos{2\theta}+i(\alpha _ 2 \sin{2\theta}-\beta _ 2 \cos{2\theta})
\end{bmatrix}
\end{aligned}
$$

と変化します.ここで

$$
\begin{aligned}
\vert \alpha' \vert ^2 &= \alpha _ 1^2\cos^2{2\theta}+2\alpha _ 1\beta _ 1\sin{2\theta}\cos{2\theta}+\beta _ 1^2\sin^2{2\theta}+\alpha^2 _ 2 \cos^2{2\theta}+2\alpha _ 2\beta _ 2\sin{2\theta}\cos{2\theta}+\beta^2 _ 2\sin^2{2\theta} \newline
&= \vert \alpha \vert ^2 \cos^2{2\theta} + \vert \beta \vert ^2 \sin^2{2\theta} + 2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta} \newline
\vert \beta' \vert ^2 &= \alpha _ 1^2\sin^2{2\theta}-2\alpha _ 1\beta _ 1\sin{2\theta}\cos{2\theta}+\beta _ 1^2\cos^2{2\theta}+\alpha^2 _ 2 \sin^2{2\theta}-2\alpha _ 2\beta _ 2\sin{2\theta}\cos{2\theta}+\beta^2 _ 2\cos^2{2\theta} \newline
&= \vert \alpha \vert ^2 \sin^2{2\theta} + \vert \beta \vert ^2 \cos^2{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
\alpha' \beta'^\ast &= \alpha^2 _ 1\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 1\sin^2{2\theta}-\beta^2 _ 1\sin{2\theta}\cos{2\theta}+\alpha^2 _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 2\cos^2{2\theta}+\alpha _ 2\sin^2{2\theta}-\beta^2 _ 2\sin{2\theta}\cos{2\theta} \newline
&+i(-\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\beta _ 2\cos^2{2\theta}-\alpha _ 2\beta _ 1\sin^2{2\theta}+\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 2\sin^2{2\theta}-\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}) \newline
\end{aligned}
$$

となりますが

$$
\alpha \beta^\ast = \alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2+i(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)
$$

であるのでこれを使うと

$$
\begin{aligned}
\vert \alpha' \vert ^2 &= \vert \alpha \vert ^2 \cos^2{2\theta} + \vert \beta \vert ^2 \sin^2{2\theta} + 2Re(\alpha \beta^\ast)\sin{2\theta}\cos{2\theta} \newline
\vert \beta' \vert ^2 &= \vert \alpha \vert ^2 \sin^2{2\theta} + \vert \beta \vert ^2 \cos^2{2\theta}-2Re(\alpha \beta^\ast)\sin{2\theta}\cos{2\theta} \newline
\alpha' \beta'^\ast &= \alpha^2 _ 1\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 1\sin^2{2\theta}-\beta^2 _ 1\sin{2\theta}\cos{2\theta}+\alpha^2 _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 2\cos^2{2\theta}+\alpha _ 2\sin^2{2\theta}-\beta^2 _ 2\cos^2{2\theta} \newline
&+i(-\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\beta _ 2\cos^2{2\theta}-\alpha _ 2\beta _ 1\sin^2{2\theta}+\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 2\sin^2{2\theta}-\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta})
\end{aligned}
$$

$$
\alpha' \beta'^\ast=(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos{4\theta}-\alpha _ 2\beta _ 2\cos{4\theta}+i(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)
$$

$$
\begin{aligned}
\vec{S'} &= 
\begin{bmatrix}
\vert \alpha' \vert ^2 - \vert \beta' \vert ^2 \newline
2 Re( \alpha' \beta'^ \ast) \newline
-2 Im( \alpha' \beta'^ \ast)
\end{bmatrix} \newline
&=
\begin{bmatrix}
(\vert \alpha' \vert ^2 - \vert \beta' \vert ^2)(\cos^2{2\theta}-\sin^2{2\theta})+4Re(\alpha \beta ^\ast) \sin{2\theta}\cos{2\theta} \newline
2(\alpha^2 _ 1+\alpha^2 _ 2)\sin{2\theta}\cos{2\theta}-2(\beta^2 _ 1+\beta^2 _ 2)\sin{2\theta}\cos{2\theta}-2\alpha _ 1\beta _ 1(\cos^2{2\theta}-\sin^2{2\theta})-2\alpha _ 2\beta _2(\cos^2{2\theta}-\sin^2{2\theta}) \newline
-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)
\end{bmatrix} \newline
&=
\begin{bmatrix}
S _ 1\cos{4\theta}+S _ 2 \sin{4\theta} \newline
S _ 1 \sin{4\theta}-S _ 2 \cos{4\theta} \newline
-S _ 3
\end{bmatrix} \newline
\therefore \vec{S'} &=
\begin{bmatrix}
\cos{4\theta} & \sin{4\theta} & 0 \newline
\sin{4\theta} & -\cos{4\theta} & 0 \newline
0 & 0 & -1
\end{bmatrix}
\begin{bmatrix}
S _ 1\newline
S _ 2\newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

と計算できます. -->

光を $\theta$ 傾けた1/2波長板によって変調するとストークスパラメーターを上式のように変換することを意味しています.つまりポアンカレ球上の $S _ 1-S _ 2$ 平面で $2\theta$ だけ方位角が反時計回りに回転し $z$ 成分の符号が反転します.

例えば $x$ 偏光ビームを $\frac{\pi}{8}$ 傾けた1/2波長板に入射させると

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1\newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
\end{aligned}
$$

と $\frac{\pi}{4}$ 傾いた直線偏光になります.

## 1/4波長板

同様に1/4波長板について考えます.

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix} &=
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha (1 - i\cos{2\theta}) - i\beta \sin{2\theta} \newline
-i\alpha \sin{2\theta} + \beta (1 + i\cos{2\theta})
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha -i(\alpha \cos{2\theta} + \beta \sin{2\theta}) \newline
\beta - i(\alpha \sin{2\theta} - \beta \cos2\theta{})
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\begin{bmatrix}
\alpha _ 1+\alpha _ 2\cos{2\theta}+\beta _ 2\sin{2\theta}+i(\alpha _ 2-\alpha _ 1\cos{2\theta}-\beta _ 1\sin{2\theta}) \newline
\beta _ 1+\alpha _ 2\sin{2\theta}-\beta _ 2\cos{2\theta}+i(\beta _ 2-\alpha _ 1\sin{2\theta}+\beta _ 1\cos{2\theta})
\end{bmatrix} \newline
\end{aligned}
$$

となります.よって

$$
\begin{aligned}
\vert \alpha'\vert^2
&=
\vert \alpha \vert^2+\vert \beta \vert^2 \sin^2{2\theta}+\vert \alpha \vert^2 \cos^2{2\theta}+2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}+2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\sin{2\theta} \newline
\vert \beta'\vert ^2
&= \vert \beta \vert^2+\vert \alpha \vert^2 \sin^2{2\theta}+\vert \beta \vert^2 \cos^2{2\theta} -2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
\alpha'\beta'^\ast
&=
\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2+(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\cos{2\theta}-(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{4\theta} \newline
&+i((\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{2\theta})
\end{aligned}
$$

となります.

$$
\begin{aligned}
\vec{S'} &= 
\begin{bmatrix}
\vert \alpha' \vert ^2 - \vert \beta' \vert ^2 \newline
2 Re( \alpha' \beta'^ \ast) \newline
-2 Im( \alpha' \beta'^ \ast)
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1+\cos{4\theta})(\vert \alpha \vert ^2 - \vert \beta \vert ^2)-4(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)\sin{2\theta}+4(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2+(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\cos{2\theta}-(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{4\theta}) \newline
-2((\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{2\theta})
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1+\cos{4\theta})S _ 1+2S _ 2\sin{2\theta}\cos{2\theta}+2S _ 3\sin{2\theta} \newline
S _ 1\sin{4\theta}+S _ 2(1-\cos{4\theta})-2S _ 3\cos{2\theta} \newline
-2S _ 1\sin{2\theta}+2S _ 2\cos{2\theta}
\end{bmatrix} \newline
\therefore \vec{S'} &=
\begin{bmatrix}
1+\cos{4\theta} & \sin{4\theta} & 2\sin{2\theta} \newline
\sin{4\theta} & 1-\cos{4\theta} & -2\cos{2\theta} \newline
-2\sin{2\theta} & 2\cos{2\theta} & 0
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
=2\begin{bmatrix}
\cos^2{2\theta} & \sin{2\theta}\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta}\cos{2\theta} & \sin^2{2\theta} & -\cos{2\theta} \newline
-\sin{2\theta} & \cos{2\theta} & 0
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

と計算できます.先ほどの1/2波長板と違って自分はどのようなパターンで変化させているか(自分は)イメージがつかめません.

### 直線偏光子

同様に考えます.

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=
\begin{bmatrix}
\cos^2{\theta} & \sin{\theta}\cos{\theta} \newline
\sin{\theta} & \sin^2{\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha \cos^2{\theta}+\beta \sin{\theta} \cos{\theta} \newline
\alpha \sin{\theta} \cos{\theta} & \beta \sin^2{\theta}
\end{bmatrix} \newline
\therefore
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=
\begin{bmatrix}
\alpha _ 1 \cos^2{\theta}+\beta _ 1 \sin{\theta} \cos{\theta}+i(\alpha _ 2 \cos^2{\theta}+\beta _ 2\sin{\theta} \cos{\theta}) \newline
\alpha _ 1 \sin{\theta} \cos{\theta}+\beta _ 1 \sin^2{\theta}+i(\alpha _ 2 \sin{\theta} \cos{\theta}+\beta _ 2\sin^2{\theta})
\end{bmatrix}
\end{aligned}
$$

であるので

$$
\begin{aligned}
\vert \alpha' \vert^2
&=
\alpha^2 _ 1\cos^4{\theta}+2\alpha _ 1 \beta _ 1\sin{\theta} \cos^3{\theta}+\beta^2 _ 1\sin^2{\theta} \cos^2{\theta}+\alpha _ 2 \cos^4{\theta}+2\alpha^2 _ 2 \beta _ 2 \sin{\theta} \cos^3{\theta}+\beta^2 _ 2\sin^2{\theta} \cos^2{\theta} \newline
\therefore
\vert \alpha' \vert^2
&=
\vert \alpha \vert^2 \cos^4{\theta}+\vert \beta \vert^2 \sin^2{\theta} \cos^2{\theta}+2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2)\sin{\theta}\cos^3{\theta}
\end{aligned}
$$

$$
\begin{aligned}
\vert \beta' \vert^2
&=
\alpha^2 _ 1\sin^2{\theta} \cos^2{\theta}+2\alpha _ 1 \beta _ 1\sin^3{\theta} \cos{\theta}+\beta^2 _ 1\sin^4{\theta}+\alpha^2 _ 2 \sin^2{\theta} \cos^2{\theta}+2\alpha _ 2 \beta _ 2 \sin^3{\theta} \cos{\theta}+\beta^2 _ 2\sin^4{\theta} \newline
\therefore
\vert \beta' \vert^2
&=
\vert \alpha \vert^2 \sin^2{\theta} \cos^2{\theta}+\vert \beta \vert^2 \sin^4{\theta}+2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2)\sin^3{\theta}\cos{\theta}
\end{aligned}
$$

$$
\begin{aligned}
\alpha \beta^\ast
&=
\alpha _ 1 \cos^2{\theta}+\beta _ 1 \sin{\theta} \cos{\theta}+i(\alpha _ 2 \cos^2{\theta}+\beta _ 2\sin{\theta} \cos{\theta}) \times \bigl(\alpha _ 1 \sin{\theta} \cos{\theta}+\beta _ 1 \sin^2{\theta}-i(\alpha _ 2 \sin{\theta} \cos{\theta}+\beta _ 2\sin^2{\theta})\bigr)
\end{aligned}
$$
