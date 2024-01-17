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
C:
---
# PA - Modes et fréquences propres dans les tubes et les cordes
Date: [[2023-12-04]] - [[2023-12-05]] 
## Équation des ondes (de d'Alembert XVIIIème) 1D
On appelle grandeur ondulatoires " $\mathbf{g}$ " qui est propagée par une onde de célérité $\mathbf{C}$ dans $(0,x)$ une seule direction, toute fonction de " $x$ et de " $t$ telle que $$\boxed{\mathbf{g}(x,t)=g(x',t')\Leftrightarrow\frac{|x-x'|}{t'-t}=\mathbf{C}}$$ (en supposant $t'>x$ )
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
Si une onde est quelconque (si une partie se déplace dans le sens positif et une partie dans le sens négative) (pour partie progressive et pour partie régréssive) , alors les grandeurs ondulatoires qu'elle transporte sont de la forme $f(x,t)=f_1(x+Ct)+f_2(x-Ct)$ .D'Alembert frappé par la grâce divine parvient à l'équivalence suivante : $f(x,t)=f_1(x+Ct) +f_2(x-Ct)\Leftrightarrow \frac{\partial^2f}{\partial.x^2} - \frac{1}{C^2}.\frac{\partial^2f}{\partial.t^2}=0$
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

>[!note]
>D'un point de vue **Thermodynamique**
On dit que les volumes : Sdx et $S(x+dx+s(x+dx,t)-(x+s(x,t)))$ et $S(dx+s(x+dx,t)-s(x,t))$ Contiennent la même masse d'air mais pas à la même pression : Sdx est à $P_{atm}$; tandis que l'autre est à $P_{atm} +p(x,t)$

En résumé, du point de vue mécanique, la fonction de pression et de déplacement acoustique dans le tube sont reliés par l'équation : $$\boxed{\frac{\partial.P}{\partial.x}=-\rho\frac{\partial^2s}{\partial.t^2}}$$ Avec $p(x,t)$ et $s(x,t)$
Aussi pour obtenir plus d'informations sur l'une ou l'autre de ces 2 fonctions, en particulier sur $p$ il faut au moins trouver une autre équation qui relie $s$ et $p$. C'est en utilisant une loi de thermodynamique, la loi de "compressibilité isentropique", que l'on peut déterminer cette équation. Selon cette loi, il existe pour chaque gaz un coefficient de compressibilité isentropique noté $\chi_s$  Qui tel que $\chi_s = -\frac{V_1-V_0}{V_0\Delta P}$ où $\Delta P$ représente la variation de pression subie par le gaz à entropie constante ce qui provoque le changement de volume de $V_0$ à$V_1$ en $m^3$.

Donc quand on passe de $V_0$ à $V_1$, $P_0\rightarrow P_1>P_0$ , Donc augmentation de pression à entropie constante induit $\Delta P = P_1 -P_0$ Ce qui donne $\chi_s = - \frac{\frac{V_1-V_0}{V_0}}{\Delta P}$ 
Quand on augmente la pression, le volume diminue, ce qui explique le signe "-". 
La compressibilité de l'air (dépendant de la température) est de : $10^{-5}$ à $10^{-6}$ (Masse volumique de l'air $1,3kg/m^3$) 

Exemple : $\chi_{sAIR}=\frac{1}{1,3.340^2}\approx7.10^{-6} Pa^{-1}$ 
Par rapport aux précédentes équation de la mécanique on retrouve : $V_0 = Sdx$; $V_1=s(x,t)$ et $\Delta P = p(x,t)$ 

$l_1= (x+dx+s(x+dx,t))-(x+s(x,t))=dx +s(x+dx,t)-s(x,t)$
$V_1 = S(dx+s(x+dx,t)-s(x,t))\Rightarrow V_1-V_0=S(s(x+dx,t)-s(x,t))$ 
Cette différence de volume est du à l'arrivée de $p(x,t)$ : 
$V_0$ était à la pression atmosphérique $P_{atm}$, 
$V_1$ est à la pression atmosphérique$P_{atm} + p(x,t)$
Du coup, la variation de pression $\Delta P$ qui provoque la variation de volume n'est autre que : $\boxed{P_{atm}+p(x,t)-P_{atm} = p(x,t)}$ soit Pression dans V0 - Pression dans V0 = p(x,t). Et en la supposant isentropique, on peut écrire : $$\boxed{\chi_s=-\frac{S(s(x+dx,t)-s(x,t))}{dxS}\Rightarrow\chi_s=-\frac{s(x+dx,t)-s(x,t)}{dx}.\frac{1}{p(x,t)}}$$
Et quand $dx\rightarrow 0$ Alors $-\frac{s(x+dx,t)-s(x,t)}{dx}$ devient $\frac{\partial s}{\partial x}(x,t)$ 
Comme c'est valable $\forall$ $x$ ou $t$, Donc cette égalité est vraie $\forall$ $x$ et $\forall$ $t$ . 
Ainsi le nombre $\chi_s.p(x,t) = -\frac{\partial s}{\partial x}(x,t)$ , l'orque l'on est au voisinage de $x$ mais c'est pour $x$ et $t$ quelconque. 

Finalement l'étude thermodynamique permet d'établir un autre lien entre les 2 fonctions $p(x,t)$ et $s(x,t)$ qui est : $$\boxed{\chi_s.p=-\frac{\partial s}{\partial x}}$$ On a donc deux relations qui doivent coexister : 
- $\chi_s p = -\frac{\partial s}{\partial x}$ *THERMO*
- $\frac{\partial p}{\partial x}=-\rho\frac{\partial^2s}{\partial t^2}$ *MÉCA*
Donc on va chercher à combiner ses deux fonctions. Cependant il n'y a pas de variable équivalents, on a 4 fonctions. On va être obligé de tenir compte des opérateurs de dérivation. 
D'après le théorème de Schwartz, l'ordre chronologique des dérivations  d'une fonction de plusieurs variable, n'influence pas le résultat de ces dérivations : la fonction dérivée partielle obtenue.
==Exemple== $f(x,y,z)\longrightarrow\frac{\partial f}{\partial x}\longrightarrow \frac{\partial\frac{\partial f}{\partial x}}{\partial z}\longrightarrow\frac{\partial\frac{\partial\frac{\partial f}{\partial x}}{\partial z}}{\partial y}$ = $f^{3}(x,y,z)$ 
La fonction obtenue $f^{3}(x,y,z)$ Pourrait être obtenue en changeant l'ordre chronologique des trois variations : $f(x,y,z)\longrightarrow\frac{\partial f}{\partial z}\longrightarrow \frac{\partial\frac{\partial f}{\partial z}}{\partial x}\longrightarrow\frac{\partial\frac{\partial\frac{\partial f}{\partial z}}{\partial x}}{\partial y}$ = $f^{3}(x,y,z)$ 
*Application* : 
$f(x,t)=3t^2x3+\sin(t)\cos(x)$ 
$\frac{\partial f}{\partial x}(x,t = 9t^2x^2-\sin(t)\sin(x)\Rightarrow\frac{\partial^2f}{\partial t\partial x}(x,t)=18tx^2+\cos{t}\sin{x}$
$\frac{\partial f}{\partial t} = 6tx^3+\cos(t)\cos(x) \Rightarrow\frac{\partial^2f}{\partial x\partial t}(x,t)=18tx^2+\cos{t}\sin{x}$
Donc les fonctions sont égale, donc l'ordre chronologique n'influence pas le résultat.

>[!note]
>$\partial x \partial t$ veut dire qu'on dérive $ t $ puis $ x $ 

Revenons à nos deux équations : 
- $\chi_s p = -\frac{\partial s}{\partial x}$ $\Rightarrow\frac{\partial^3s}{\partial t\partial t\partial x}=-\chi_s\frac{\partial^2p}{\partial t^2}$
- $\frac{\partial p}{\partial x}=-\rho\frac{\partial^2s}{\partial t^2}$ $\Rightarrow\frac{\partial^3s}{\partial x\partial t^2}=-\frac{1}{\rho}\frac{\partial^2p}{\partial x^2}$
Par le théorème de Schwartz les deux fonctions dérivées 3ème de s sont égales et donc $-\chi_s\frac{\partial^2p}{\partial t^2}=-\frac{1}{\rho}\frac{\partial^2p}{\partial x^2}$ 
On obtient l'équation que la fonction de la pression $p$ doit vérifier (à elle toute seule)
$$\boxed{\frac{\partial^2p}{\partial x^2}-\rho\chi_s\frac{\partial^2p}{\partial t^2}= 0}$$ Ce qui est donc l'équation de d'Alembert si $\rho\chi_s = \frac{1}{C^2}$ Et si $\rho\chi_s$ s'exprime en $\frac{1}{(m/s)^2}$ 
Si on peut démontrer sa, ça veut dire que g est transporté par une onde. (g ici étant p){démontrée ici*}

Grâce à la synthèse des 2 équations obtenues, en utilisant le Principe Fondamental de la Dynamique (PFD) pour l'une et la compressibilité isentropique pour l'autre, on peut affirmer que la pression acoustique dans le tube est modélisa le par une fonction de $x$ et de $t$ vérifiant : $\frac{\partial^2p}{\partial x^2}-\rho\chi_s\frac{\partial^2p}{\partial t^2}= 0$ 
Or $\rho$ s'exprime en $kg/m^3$ et $\chi_s en $Pa^{-1}$. Donc $\rho.\chi_s$ s'exprime en $\frac{kg}{m^3.Pa}$. Mais le $Pa$ n'est autre que le $\frac{N}{m^2}$ et le $N$euton n'est autre que le $kg.m/s^2$ (d'après la thermodynamique); tant est si bien que $\frac{kg}{m^3.Pa} =\frac{kg}{m^3.\frac{N}{m^2}}=\frac{kg}{m^3.\frac{kg.m}{m^2.s^2}}$
Donc $\rho\chi_s$ s'exprime en $\frac{kg}{\frac{m^2.kg}{s^2}}=\frac{1}{(m/s)^2} (=\frac{s^2}{m^2})$
$\rho\chi_s$ est homogène au carré de l'inverse d'une vitesse ( $m/s$ ), ce qui revient à dire qu'il existe une vitesse $\mathbf{C}$, telle que $\rho\chi_s = \frac{1}{\mathbf{C}^2}$ 
La célérité du son apparaît ici comme étant égale à : $\boxed{\mathbf{C}=\frac{1}{\sqrt{\rho\chi_s}}}$ 

#### Vérification en partant de l'équation de déplacement :
[[Sophie Germain]] : Première femme mathématicienne et physicienne à avoir du publier en son nom. Deux travaux majeurs : à apporter des connaissances sur le théorème de Fermat. 
[[Pierre de Fermat]] Juriste passionné de mathématique. Il s'intéresse aux mathématiques et à la physique durant son temps libre. Il va découvrir un des principes de bases de l'optique géométrique. Il a permis l'explication des lois de Décartes. Il n'y a aucune fautes dans ses écrits (singularité). Quand il trouvait un truc il ne donnait pas sa démonstration il l'envoyait simplement le résultat à ses contemporain. 
Le théorème de Fermat, il l'a prouvé, mais il n'a pas dis comment il l'a prouvé → Tous les mathématiciens se sont cassé les dents dessus, car tout ce qu'il disait se trouvait être vrais. Il a été prouvé en 1994 par pierre Willes, longtemps après. 
Sophie germain va participer à l'explication de ce théorème. 
Elle va aussi travailler sur les plaques vibrantes : un objets soumis à des ondes stationnaires. Sophie a su tenir en compte l'épaisseur de la plaque. Elle a su modéliser les plaque en 3D contrairement à avant on on ne pouvait le penser qu'en 2D. 

Elle a donc fait avancer la connaissance sur un des théorème les plus complexe et. De l'acoustique. Ce qui a donner de la crédibilité sur la science acoustique. 
C'est en fusionnant les deux points de vue que l'on peut comprendre la science des vibrations (acoustiques). Elle occupe une place à part entière car elle réalise la synthèse de deux phénomènes.

La fois prochaine on verra ce qui se passe quand on définit une longueur de tube fixe. 
#### Rappel 
La pression acoustique dans un tube de longueur indéfinie est modélisable par une fonction $p(x,t)$ qui vérifie l'EDP de d'Alembert $$\frac{\partial ^2 p}{\partial x^2}-\frac{1}{C^2}.\frac{\partial^2 p}{\partial t^2}=0$$

On doit à [[Laplace]] la résolution de cette équation dans le cas où le tube est de longueur finie L (en m) pour chaque "sous-cas" de CLCI (Conditions aux Limites & Condition Initiale)

##### Trois conditions aux limites possibles : 

1. Tube fermé des deux côtés
2. Tube ouvert des deux côtés 
3. Tube ouvert d'un côté et fermé de l'autre

##### Une seule condition initiale : 
À $t = 0$, $\forall\:x \in [0;L]\: p(x,0) = 0$ 

#### Résolutions
Ces trois résolution s'appuient sur la méthode dite "de séparation des variables", sur une modélisation des conditions aux limites[^1] et permet de mettre en évidence les notions de modes propres, de fréquences propres et d'onde stationnaires. 

[^1]: Condition de fermeture en $x\:=\:0$ ou en $x = L$ : $\frac{\partial\:p}{\partial\:x}(0,t)=0$ ou $\frac{\partial\:p}{\partial\:x}(L,t)=0$ 
[^1]: Condition d'ouverture en $x\:=\:0$ ou en $x = L$  : $p(0,t) = 0$ ou $p(L,t)=0$

Les développement mathématique de ces 3 résolutions sont évités ici. On en donne que les 3 résultats : 
1. Le tube fermé des deux côtés : $p(x,t) = \sum_{n=1}^{\infty} K_n \cos(\frac{n\pi}{L}\:x)\sin(\frac{n\pi}{L}\:Ct)$ Où les nombre $K_n$ restent à déterminer par l'ajout d'une condition temporelle à t=0
2. Le tube ouverts des 2 côtés : $p(x,t) = \sum_{n=1}^{\infty} K_n \sin(\frac{n\pi}{L}\:x)\sin(\frac{n\pi}{L}\:Ct)$ Où les nombre $K_n$ restent à déterminer par l'ajout d'une condition temporelle à t=0
3. Le tube est fermé en x=0 et ouvert en x=L : $p(x,t) = \sum_{n=1}^{\infty} K_n \cos(\frac{(2n+1)\pi}{2L}\:x)\sin(\frac{(2n+1)\pi}{2L}\:Ct)$ Où les nombre $K_n$ restent à déterminer par l'ajout d'une condition temporelle à t=0

>[!note]
>Dans chaque cas, il est clair que la physique impose à la somme obtenue de ne pas comporter une infinité de termes

On montre que les coefficient $K_n$ tendent vers zéros quand $n\rightarrow\infty$. Et donc chaque solution ce réduit à une somme finie pour n variant de 1 à une valeur $\mathbf{N}$ telle que $K_{\mathbf{N}};K_{\mathbf{N}+1};K_{\mathbf{N}+2}…$ etc sont, en valeur absolue, négligeables
Car le facteur multiplie l'ensemble de l'équation… On enlève les termes à partir duquel ils sont tous trop petits pour être interprétables physiquement. 
### Modes et fréquence propre du tube fermé des deux côtés 
Dans ce tube, la pression acoustique est donnée par $p(x,t)= K_1 \cos{\frac{\pi}{L}x}\sin{\frac{\pi}{L}Ct}+K_2 \cos{\frac{2\pi}{L}x}\sin{\frac{2\pi}{L}Ct}+K_3 \cos{\frac{3\pi}{L}x}\sin{\frac{3\pi}{L}Ct}+…K_{10n}$
Supposons que l'on crée une pression acoustique dans un tel tube en faisant vibrer un point du tube à une fréquence $\mathbf{F}_n$ du type $\frac{nC}{2L}$ Hz. Cette solicitation mécanique est du type $A\sin({2\pi\mathbf{F}_nt})$; c'est à dire $A\sin(\frac{n\pi}{L}Ct)$; par exemple pour n = 3 : $A\sin(\frac{3\pi}{L}Ct)$ 

De part le choix $\mathbf{F}_n=\frac{nC}{2L}$ Hz on est sûr que pour $n ≤ N$ la dépendance temporelle de la solicitation mécanique se trouve dans la somme de fonction qui constitue $p(x,t)$ 

Et les expériences montrent que lorsq'un tube fermé des deux côtés est ainsi solicité, la fonction de pression acoustique se restreint à **1 terme** de la somme : $K_n\cos(\frac{n\pi}{L}x).\sin(\frac{nπ}{L}Ct)$ : la variation temporelle de la sollicitation sinusoïdale à la fréquence $\frac{nC}{2L}$ Hz 
C'est un peu comme si tous les nombres $K_1,K_2,K_3,…,K_{n+1},K_{n+2},…,K_N$ prenaient la valeur 0. Ce phénomène physique particulier a conduit les acousticiens à qualifier le couple {$\mathbf{F}_n, cos(\frac{nπ}{L}x)sin(\frac{nπ}{L}Ct)$} d'énième {Fréquance propre et Mode propre} du tube. 

#### Illustration du mode 3 $\longrightarrow$ que l'on va généraliser au mode n
Soit $t_p$ un instant où $sin(\frac{3π}{L}Ct_p)>0$ [^2]. À cet instant la pression acoustique est répartie dans le tube selon la fonction de x : $K_3 . sin(\frac{3π}{L}Ct_p).\cos (\frac{3π}{L}x)$  = $A_{3,t_p} \cos (\frac{3π}{L}x)$
Représentons la courbe de cette fonction pour x variant de 0 à L 
![[PA - Modes et fréquences propres dans les tubes et les cordes 2024-01-12 11.50.47.excalidraw|700]]
Soit $x_1$ tel que $\cos (\frac{3π}{L}x_1)=0$
Pour la première fois : Donc $\frac{3π}{L}x_1 = \frac{π}{2}$ ce qui nous donne $x_1 = \frac{L}{6}$

SI $t_1$ est tel que $\frac{3π}{L}Ct_1 = \frac{π}{2} \Leftrightarrow t_1 = \frac{L}{6C}$ alors le sinus [^2]: vaux 1 . Alors on obtient la courbe bleue. 
Courbe verte : Pour $t_2$ tel que $\frac{3π}{L}Ct_2 = \frac{3π}{2} \Leftrightarrow t_2 = \frac{L}{6C}$. Le sinus [^2]: vaut -1 et la répartition de pression dans le tube est "à l'opposé" de celle observée à l'instant $t_1$ 
On remarque qu'au cours du temps la pression acoustique dans le tube se répartit selon une courbe toujours comprise dans un fuseau. (Cf schéma entre la courbe bleue et verte). De plus on observe qu'il existe des sections de tube ou la pression acoustique demeure nulle (noeuds). ainsi que d'autres où la pression acoustique reste en valeur absolue maximale pour un instant donnée. (Ventres)


>[!note]
>Donc si on frotte un tube a une fréquence spécifique il va réagir d'une façon singulière. On dit que ce sont les fréquences propre du tube et la variation spécifique est appelée le mode propre du tube. (Si on tape le tube, il va en sortir tout les K de la somme). 

