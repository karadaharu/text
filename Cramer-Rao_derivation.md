# Cramer-Raoの不等式の導出
## Cramer-Raoの不等式



## 導出

確率変数 $X\in \mathbb{R}$ について、未知パラメーター $\theta\in \mathbb{R}$ をもつ確率密度関数 $P(X|\theta)$ を考えます。

いま、確率変数 $X$ の標本 $\bar{X} \in \mathbb{R}^N$ が得られたとします。$\bar{X}$ が得られる確率は、 $P(\bar{X}|\theta)$ であり、 $\bar{X}$ について積分すると、

 $\int P(\bar{X}|\theta) d\bar{X} =1$ ,

 となります。上式において、両辺を $\theta$ で微分すると、

 $\frac{\partial}{\partial\theta} \int P(\bar{X}|\theta) d\bar{X} = 0$ .

微分演算子を積分の中にいれて、 $P(\bar{X}|\theta)/P(\bar{X}|\theta)=1$ をかけると、

 $\int \frac{P(\bar{X}|\theta)}{P(\bar{X}|\theta)} \frac{\partial}{\partial\theta} P(\bar{X}|\theta) d\bar{X} = 0$ .

ここで、

$\frac{1}{P(\bar{X}|\theta)} \frac{\partial}{\partial\theta} P(\bar{X}|\theta) = \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta))$ ,

であるので、

 $\int P(\bar{X}|\theta) \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta))  d\bar{X} = 0 \ .$

 上式は、$\theta$ についての対数尤度  $\log(P(\bar{X}|\theta))$ の期待値が0になることを表しています。

さらに、両辺に $\theta$ をかけると、次の式が得られます。

 $\int P(\bar{X}|\theta) \theta \frac{\partial}{\partial\theta} \log (P(\bar{X}|\theta))  d\bar{X} = 0 \ . \ \  \ \ (1)$



 次に、$\bar{X}$ から $\theta$ の不偏推定量 $\hat{\theta}$ が得られたとします。不偏推定量の定義から、 $\hat{\theta}$ の期待値は真の値 $\theta$ となります :

 $E[\hat{\theta}] = \int \hat{\theta}P(\bar{X}|\theta)d\bar{X}=\theta$ .

 上式に対し、さきほどと同様の式変形を行います。

 まず、上式の両辺を $\theta$ について微分すると、

 $\frac{\partial}{\partial \theta} \int  \hat{\theta}P(\bar{X}|\theta)d\bar{X}=1$ .

 さらに、微分演算子を積分の中にいれて、 $P(\bar{X}|\theta)/P(\bar{X}|\theta)=1$ をかけ、


 $\int \frac{P(\bar{X}|\theta)}{P(\bar{X}|\theta)} \hat{\theta} \frac{\partial}{\partial \theta}  P(\bar{X}|\theta)d\bar{X}=1$ .

 式変形すると、

 $\int P(\bar{X}|\theta) \hat{\theta} \frac{\partial}{\partial \theta}  P(\bar{X}|\theta)d\bar{X}=1\ . \ \  \ \ (2)$

 ここで、(1)式から(2)式をひくと、

 $\int P(\bar{X}|\theta) \hat{\theta} \frac{\partial}{\partial \theta}  P(\bar{X}|\theta)d\bar{X}=1\ . \ \  \ \ (2)$
