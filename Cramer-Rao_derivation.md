# Cramer-Raoの不等式の導出

## Cramer-Raoの不等式

パラメーター \(\theta\) をもつ確率密度関数 \(P(X|\theta)\) に従う確率変数 \(X\) を考えます。

観測値 \(\hat{X}\) から求めた \(\theta\) の不偏推定量 \(\hat{\theta}\) の分散について、以下の不等式が成り立ちます。

 $$E[(\hat{\theta}-\theta)^2] \geq E^{-1}[(\frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta)))^2] \ .$$

## 導出

確率変数 \(X\in \mathbb{R}\) について、未知パラメーター \(\theta\in \mathbb{R}\) をもつ確率密度関数 \(P(X|\theta)\) を考えます。

いま、確率変数 \(X\) の標本 \(\bar{X} \in \mathbb{R}^N\) が得られたとします。\(\bar{X}\) が得られる確率は、 \(P(\bar{X}|\theta)\) であり、 \(\bar{X}\) について積分すると、

 $$\int P(\bar{X}|\theta) d\bar{X} =1 \ ,$$

 となります。上式において、両辺を \(\theta\) で微分すると、

 $$\frac{\partial}{\partial\theta} \int P(\bar{X}|\theta) d\bar{X} = 0 \ .$$

微分演算子を積分の中にいれて、 \(P(\bar{X}|\theta)/P(\bar{X}|\theta)=1\) をかけると、

 $$\int \frac{P(\bar{X}|\theta)}{P(\bar{X}|\theta)} \frac{\partial}{\partial\theta} P(\bar{X}|\theta) d\bar{X} = 0 \ . $$

ここで、

$$\frac{2}{P(\bar{X}|\theta)} \frac{\partial}{\partial\theta} P(\bar{X}|\theta) = \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta)) \ , $$

であるので、

 $$\int P(\bar{X}|\theta) \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta))  d\bar{X} = 0 \ .$$

 上式は、\(\theta\) についての対数尤度  \(\log(P(\bar{X}|\theta))\) の期待値が0になることを表しています。

さらに、両辺に \(\theta\) をかけると、次の式が得られます。

 $$\int P(\bar{X}|\theta) \theta \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta))  d\bar{X} = 0 \ . \ \  \ \ (1)$$

 次に、\(\bar{X}\) から \(\theta\) の不偏推定量 \(\hat{\theta}\) が得られたとします。不偏推定量の定義から、 \(\hat{\theta}\) の期待値は真の値 \(\theta\) となります :

 $$E[\hat{\theta}] = \int \hat{\theta}P(\bar{X}|\theta)d\bar{X}=\theta \ .$$

 上式に対し、さきほどと同様の式変形を行います。

 まず、上式の両辺を \(\theta\) について微分すると、

 $$\frac{\partial}{\partial \theta} \int  \hat{\theta}P(\bar{X}|\theta)d\bar{X}=1 \ . $$

 さらに、微分演算子を積分の中にいれて、 \(P(\bar{X}|\theta)/P(\bar{X}|\theta)=1\) をかけ、

 $$\int \frac{P(\bar{X}|\theta)}{P(\bar{X}|\theta)} \hat{\theta} \frac{\partial}{\partial \theta}  P(\bar{X}|\theta)d\bar{X}=1 \ .$$

 式変形すると、

 $$\int P(\bar{X}|\theta) \hat{\theta} \frac{\partial}{\partial \theta} \log ( P(\bar{X}|\theta))d\bar{X}=1\ . \ \  \ \ (2)$$

 ここで、(2)式から(1)式をひくと、

 $$\int P(\bar{X}|\theta) (\hat{\theta}-\theta) \frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta))d\bar{X}=1 \ .$$

 これは、\((\hat{\theta} - \theta) \frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta))d\bar{X}\) の期待値を表しています :

 $$E[(\hat{\theta} - \theta) \frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta))]=1 \ .$$

 ここで、Cauchy-Schwarzの不等式から、確率変数A、Bについて、

 $$E[A^2]E[B^2] \geq (E[AB])^2$$

 が成り立つので、

 $$E[(\hat{\theta}-\theta)^2]E[(\frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta)d\bar{X}))^2] \geq (E[(\hat{\theta} - \theta) \frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta))])^2=1 \ .$$

 が成り立ちます。これを式変形すると、

 $$E[(\hat{\theta}-\theta)^2] \geq E^{-1}[(\frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta)))^2] \ .$$

 これがCramer-Raoの不等式です。

 また、 \(E[(\frac{\partial}{\partial \theta} \log (P(\bar{X}|\theta)))^2]\) をFisher 情報量と呼びます。

 ## 参考文献

 * [The online lecture by Prof. Aditya K. Jagannatham in IIT Kanpur](https://www.youtube.com/watch?v=j0Dy55ukoo4)
