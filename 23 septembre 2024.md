#cm

# Covariance et écart type

Covariance nulle != indépendant. Juste qu'il n'y a pas de dépendance **linéaire** bien qu'elle puisse être quadratique/...

Pour avoir la covariance entre X et Y on regarde **l'écart** entre X et sa moyenne, ainsi que entre Y et sa moyenne. Ce qu'on appelle un *match* est lorsque X-$\mu_{x}$ est du même signe que $Y-\mu_{y}$. Si ces matchs arrivent régulièrement, il y a corrélation.

Covariance > 0 alors il y a plus de *matches* que de "pas" matches.
Covariance < 0 alors il y a plus de "pas matches" que de *matches*.
-> CF slide 40

Attention, la covariance ne sera jamais "nulle" mais on aura plutôt une valeur proche de zéro si pas lié. On aura un autre indicateur qui permettra de voir a quel point c'est significatif ou pas.

Super important car beaucoup d'applications (il a donné un exemple mais j'ai oublié):
$$
\mathbb{V(aX + bY) = a^2V(X) + b^2V(Y) + 2abC(X,Y)}
$$

**Corrélation**: Covariance divisée par la racine du produit des écarts types des deux variables

$$
\rho_{{XY}} = \frac{\mathbb{C}(X,Y)}{\sqrt{\mathbb{V}(X)\mathbb{V}(Y)}}
$$
Si $\rho$ > 0 -> alignement croissant (au plus X est grand, au plus Y est grand) et si $\rho$ = 1 alors on a une dépendance linéaire croissante parfaite $Y = aX +b$

Idem pour < 0 mais décroissant (au plus X est grand au plus Y est petit)
Elle ne dépend pas du "scaling".

---

# Théorème Central Limite (TCL)

Ce théorème permet de démontrer énormément de choses. 

Prenons une variable aléatoire X. Si elle suit une loi *normale* alors on peut connaitre sa fonction de densité avec son espérance et sa variance. 

$$
f(x) = \frac{1}{\sigma \sqrt{ 2\pi }}\exp( -\frac{1}{2}( \frac{x-u}{\sigma})^2)
$$
note: *iid* signifie independent identically distributed. En gros on a fait la même expérience plusieurs fois. Flemme de recopie les slides pour la def du TCL.

#### Écart du prof je ne sais pas de quoi il parle lolilol
Considérons une loi $X \sim N(\mu, \sigma^2)$ et $Y = a +bX \sim N(a+b\mu, b²\sigma²)$  

$$
\frac{X-\mu}{\sigma} \sim Z \approx N(0,1)
$$
$$
Cov(X,Y) = \sigma_{XY}
$$
$$
ax + by \sim N(a\mu_{x}+b\mu_{y}, a²\sigma_{x}² + b²\sigma_{y}² + 2ab\sigma_{xy})
$$



Variance
Properties of the variance. If $X$ and $Y$ are two r.v. (discrete or continuous) and $a, b \in \mathbb{R}$, then
- $\operatorname{Var}(X)=\mathbb{E}\left(X^2\right)-(\mathbb{E}(X))^2$
- $\operatorname{Var}(a)=0$
- $\operatorname{Var}(a+b X)=b^2 \mathbb{V}(X)$
- In general, $\operatorname{Var}(X+Y) \neq \mathbb{V}(X)+\mathbb{V}(Y)$ except if $X$ and $Y$ are independent
- The proofs are let to the reader and do not present any difficulty.

If we observe $n$ outcomes of a random variable $x_i$, the empirical variance $s^2=\frac{\sum_{i=1: n}\left(x_i-\bar{x}\right)^2}{n-1}$ is used as estimator of $\sigma_X^2$ (details provided later) Numpy: np.std(X)
