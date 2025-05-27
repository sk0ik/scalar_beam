- [ストークスパラメーター](#ストークスパラメーター)
- [ポアンカレ球](#ポアンカレ球)
- [1/2波長板](#12波長板)
- [1/4波長板](#14波長板)

## ストークスパラメーター

ベクトルビームについて考える前に直線偏光,楕円偏光,円偏光などのスカラービームについて考えます.楕円偏光は直線偏光と円偏光の中間に位置するような偏光状態でその名の通り振動の軌跡が楕円になっています.以下ではこれらの分類,もしくは各偏光状態がどのようなパラメーターを持っているのかを考えます.

任意のスカラービームは２つの直交基底ベクトル(直交する偏光状態を表すベクトル)の重ね合わせで表現できます.

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

のように表されます.

## ポアンカレ球

実は計算すると分か理ますが先ほどのストークスパラメーターは

$$
S^2 _ 1 + S^2 _ 2 + S^2 _ 3 = 1
$$

の関係があります.

これはストークスベクトルが

 $S_1, S_2, S_3$ **を軸とした単位球面上の1点を指している.**

ということを表しています.

そのように考えると

**波長板によって光の偏光分布が変わるということはジョーンズベクトルが変わる、つまりストークスベクトルが変わる、つまりポアンカレ球面上で別の座標に移る.**

ということを意味しています.具体的には

**波長板によってポアンカレ球上の座標がくるくると移動するということ.**

です.

※このように長さを変えない(今は球の表面上で移動する)写像を等長写像といいます.

水平偏光が $(S_1, S_2, S_3) = (1, 0, 0)$

右回り円偏光が $(S_1, S_2, S_3) = (0, 0, 1)$

などのように1点で表すことができます.

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

と計算できます.

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
