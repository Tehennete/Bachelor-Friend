---
Matière:
  - Psychoacoustique
Semestre:
  - B2-1
Date: 2023-12-04
Prof: "[[Laurent Allard]]"
Type: notes de cours
tags:
  - cours
  - Psychoacoustique
---
# PA - Modes et fréquences propres dans les tubes et les cordes
Date: [[2023-12-04]] 
## Équation des ondes (de d'Alembert XVIIIème) 1D
On appelle grandeur ondulatoires "$\mathbf{g}$" qui est propagée par une onde de célérité $\mathbf{C}$ dans $(0,x)$ une seule direction, toute fonction de "$x$ et de "$t$ telle que $$\boxed{\mathbf{g}(x,t)=g(x',t')\Leftrightarrow\frac{|x-x'|}{t'-t}=\mathbf{C}}$$ (en supposant $t'>x$)
Il y a trois cas possibles : 
- La propagation de l'onde (à la célérité C en m/s) s'effectue dans le sens de $x$ croissant
- La propagation de l'onde (à la célérité C en m/s) s'effectue dans le sens de $x$ décroissant
- La propagation de l'onde (à la célérité C en m/s) s'effectue dans les deux sens

>[!note]
>$\mathbf{v}(x,t)≠ \mathbf{C} (340m/S)$
>La vitesse acoustique est différente de la Célérité.
>Analogie du train, la vitesse du train c'est la célérité, et quand les wagons bougent pendant que le train fonctionne (petits coups, variations, oscillations) et qu'ils se transmettent de wagon en wagon c'est la vitesse "acoustique"

### Ondes progressive
![[PA - Modes et fréquences propres dans les tubes et les cordes 2023-12-04 13.36.31.excalidraw]]
g reprendra sa valeur $g(x,t)$ c'est à dire $g(x',t')=g(x,t)$ est conditionnée par : $\mathbf{C} = \frac{x'-x}{t'-t}$

On a $C[t'-t]=x'-x$
$\Rightarrow Ct'-Ct = x'-x$
$\boxed{x-Ct=x'-Ct'}\Longrightarrow$ 
- $x-Ct$ : Variable spatio-temporelle PROGRESSIVE 
- $g(x,t)$ ne peut pas dépendre de $x$ et de $t$ n'importe comment 

Exemple : $g(x,t)= (x-ct)^2.e^{-\frac{(x-ct^3)}{5}}$
Contre exemple : $f(x,t)= x^2-3t^4$

### Ondes régressive
Pour une onde regressive la variable spacio-temporelle est $x+Ct$ . Les grandeurs doivent être en fonction de $x+Ct$.
Si une onde est quelconque (si une partie se déplace dans le sens positif et une partie dans le sens négative) (pour partie progressive et pour partie régréssive) , alors les grandeurs ondulatoires qu'elle transporte sont de la forme $f(x,t)=f_1(x+Ct)+f_2(x-Ct)$.D'Alembert frappé par la grâce divine parvient à l'équivalence suivante : $f(x,t)=f_1(x+Ct) +f_2(x-Ct)\Leftrightarrow \frac{\partial^2f}{\partial.x^2} - \frac{1}{C^2}.\frac{\partial^2f}{\partial.t^2}=0$
Ou $\frac{\partial^2f}{\partial.x^2}$ représente la dérivée (partielle) de $f$ par rapport à $x$ deux fois;
Et  $\frac{\partial^2f}{\partial.t^2}$ représente la dérivé (partielle) de $f$ par rapport à $t$ deux fois

partial d
Démon
#### Rappels Dérivés 
Théorème de la dérivation des fonctions composées
$f(g(x))'=g'(x)f'(g(x))$

Exemple : 
$sin(3x^2+4x)'=(6x+4).cos(3x^2+4x)$ car g(x)$\Rightarrow$ g'(x) = 6x+4 et sin'(u)=cos(u)

##### Additions
$(f(x)+g(x))'=f'(x)+g'(x)$

Exemple : $F(x,y)= x^4.y^3+2x.y^3$ donnera 
- $= 4x^3.y^3 + 2y^3$
- $=3x^4.y^2 + 6x.y^2$

Soient $u=x-Ct$ ; $v=x+Ct$

$\frac{\partial.f}{\partial.x}(x,t)= \frac{\partial.f_1}{\partial.x}(x,t)+\frac{\partial.f_2}{\partial.x}(x,t)$ ; $\frac{\partial^2f}{\partial.x^2}(x,t)= 1.1.f_1''(v)+1.1.f_2''(u) = f_1''(u)+f_2''(v)$
Or $f_1(x_1,t)=f(x+Ct)=f'(v)$  Et $f_2(x,t)=f_2(x-Ct)=f_2(u)$ 

$\frac{\partial.f}{\partial.t}(x,t)=\frac{\partial.f_1}{\partial.t}(x,t)+\frac{\partial.f^2}{\partial.t}(x,t)= Cf_1'(v)+(-C)f_2'(u)$

$\frac{\partial.f}{\partial.t}(x,t)=\frac{\partial.f_1}{\partial.t}(x,t)+\frac{\partial.f^2}{\partial.t}(x,t)= Cf_1'(v)+(-C)f_2'(u)$

## I) Propagation guidée de la pression acoustique dans un tube de section constante S
#### Mécanique 
![[PA - Modes et fréquences propres dans les tubes et les cordes 2023-12-04 14.40.00.excalidraw|500]]
En $x$ et à $t$, il y a $P_{atm} + p(x,t)$
Et en $x+dx$ et à l'instant $t$, il y a $P_{atm}+p(x+dx,t)$

La masse de fluide (air) contenue dans le volume Sdx subit deux forces différentes  : 
$\overrightarrow{F}(x,t)=S.p(x,t)\vec{i}$ et $\overrightarrow{F}(x+dx,t)= S.p(x+dx,t)(-\vec{i})$. A cause de ces forces, cette masse est accélérée. Et comme on a définit une fonction s(x,t) de déplacement acoustique, on a :  $\vec{a}(x,t)=\frac{\partial^2s}{\partial.t^2}(x,t)\vec{i}$  (Accélétation )
Donc le principe Fondamental de la Dynamique (PFD) $\Rightarrow$ $S.p(x,t)-S.p(x+dx,t) = \rho dx\frac{\partial^2s}{\partial.t^2}(x,t)\vec{i}$  (La masse x l'accélération = Somme des forces)

$\frac{p(x+dx,t)-p(x,t)}{dx}=-\rho\frac{\partial^2s}{\partial.t^2}(x,t)$
Or quand dx $\rightarrow$ 0 (Vrai pour tous $\forall x$ et $\forall t$) car $f'(x)=\lim\limits_{x\to0} [\frac{f(x+h)-f(x)}{h}]$

$\frac{\partial.p}{\partial.x}(x,t)= -\rho\frac{\partial^2s}{\partial.t^2}(x,t)$
Donc $$\boxed{\frac{\partial.p}{\partial.x}=-\rho\frac{\partial^2s}{\partial.t^2}}$$

#### Thermodynamique
On dit que les volumes : Sdx et $S(x+dx+s(x+dx,t)-(x+s(x,t)))$ et $S(dx+s(x+dx,t)-s(x,t))$ Contiennent la même masse d'air mais pas à la même pression : Sdx est à $P_{atm}$; tandis que l'autre est à $P_{atm} +p(x,t)$
