---
Matière: Physique
Semestre: B2-1
Date: 2023-10-31
Prof: Rakotoniaina
Type: notes de cours
tags:
  - cours
  - physique
---
# Acoustique Architecturale
Date: [[2023-10-31]] 

### Petit rappel 
Quand le son se propage dans l'air, il rencontre divers phénomènes. 
Avec le vent il va subir un phénomène de réfraction
![[Pasted image 20231031153334.png|500]]
En première année on a analysé principalement des son en champ libre.  On va maintenant étudier des sons en champs réverbérés. 
![[Pasted image 20231031154033.png]]

## Généralités
Deux types de réflexions caractérise le timbre perçu
- Réflexion précoces ou première réflexions: intensité issue des premières réflexions qui suivent le son direct et dans la distribution temporelle est irrégulière
- Réflexion en champ diffus : Intensité acoustique issue de multiples réflexions dont la densité ne permet plus de dissocier les différentes composantes temporelles du son

## Phénomène sonore dans une salle
Lorsqu'une onde se propage, elle subit un *certain* nombre de phénomènes dans l'air et sur les parois.
→ *Dans l'air l'onde* est soumise à l'atténuation géométrique (par rapport à la distance) et à l'atténuation par dissipation (en fonction de la température et de l'humidité), ainsi qu'un phénomène de réfraction (rappelons que dans une salle, la réfraction tend notamment à dévier les ondes sonore en direction du plafond, c'est l'inversion de température, le mistral etc…).
→ *Lorsque l'onde rencontre une paroi*, Une partie de l'énergie est réfléchie et une partie est absorbée (on ne tient pas compte ici de la transmission d'une salle à l'autre, qui sera traité au chapitre 4). Il peut y avoir de la diffraction, c'est à dire un changement de direction de l'onde provoquée par un obstacle. 

![[Pasted image 20231031160426.png|500]]

>[!note]
>Le phénomène de diffraction se manifeste lorsque l'onde traverse un trou de dimension plus petite que la longueur d'onde du signal. 
## Bilan Énergétique
Soit une onde qui frappe une paroi. Définissons les grandeurs suivantes :
→ Énergie incidente ($E_i$) : l'énergie de l'onde qui frappe la paroi 
→ Énergie absorbée ($E_a$) : L'énergie transformé en chaleur dans la surface absorbante
→ Énergie transmise ($E_t$) : Une partie  ($E_t$) de l'énergie incidente peut être transmise de l'autre côté de la paroi, grâce à la vibration de celle-ci. 
→ Énergie réfléchie ($E_r$) : L'énergie renvoyée par la surface. 

Or l'énergie se conserve donc : $$\boxed{E_i = E_a + (E_t + E_r)}$$ On ne va pas utiliser l'énergie mais des coefficient tels que 
Le coefficient d'absorption $\alpha$ tel que $\alpha = \frac{E_a}{E_i}$
Le coefficient de transmission de transmission sera appelé *t* tel que : $t = \frac{E_t}{E_i}$
Le coefficient de réflexion *r* tel que : $r = \frac{E_r}{E_i}$
Avec la somme des 3 : $$a + r + t = 1$$
## Absorption
### Principe 
L'orque qu'un onde sonore rencontre une paroi, une partie de l'énergie peut être absorbée : c'est le phénomène d'absorption acoustique. Et cette énergie absorbée est transformée en chaleur.
### Coefficient d'absorption
L'absorption d'un matériau est mesuré par son coefficient d'absorption que l'on notera $\alpha$ : ($0 < \alpha < 1$ )

On ne va pas travailler avec l'énergie car c'est trop complexe, on va plutôt utiliser le coefficient d'absorption *a* tel que : $a = \frac{E_a}{E_i}$
Si $\alpha = 1$ : C'est une porte/fenêtre *ouverte*

>[!note]
>Le coefficient d'absorption d'un matériau dépend de la fréquence de l'onde sonore et de l'angle d'incidence 

>[!note]
>Le bois dispose d'un coefficient quasiment identique sur toute les fréquences.

## Aire équivalente d'absorption 
### absorption $A_i$ $(m^2)$ d'une surface $S_i$
Exemple : le tableau de la classe fait $2m x 1m = 2m^2$
Si il est en bois d'après la tableau de valeur du polycopié : $\alpha = 0,1$ (10% d'absorption)
Son aire équivalente sera : $A_i = S_i \times \alpha = 2 \times 0,1 = 0,2$ 
#### Absorption équivalente d'une salle
Dans le cas de pièce parallélépipède, on pourra, en faisant la somme des 6 Aires équivalente, obtenir l'Aire d'absorption équivalente totale.
$$\boxed{A_{tot} = A_1 + A_2 + A_3 +...+ A_6}$$
Avec $A_1 = S_1 \times \alpha_1$, $A_2 = S_2 \times \alpha_2$ etc….  
### Coefficient d'absorption moyen
Le $\alpha_{moy}$ sera le coefficient de l'aire équivalente d'une pièce : $\boxed{\alpha = \frac{A_{tot}}{S_{tot}}}$ 
*Exemple :* Calculer le coefficient d'absorption moyen d'une salle parallélépipèdique de dimension L = 20m, l = 10m et h = 3m, recouverte des matériaux suivants. Les murs sont en plâtres, de clef d'absorption A = 0,20, le sol en parquet avec a=0,10 et le plafond en béton brute avec  a = 0,02.  
$A_{mur} = (2 \times L \times h + 2 \times l \times h) \times \alpha_{mur}$ = (2 x 20 x 3 + 2 x 10 x 3) x 0,20 = 
$A_{Plafond} = L \times l \times \alpha_{plafond}$ = 20 x 10 x 0,02 = 
$A_{Sol} = L \times l \times \alpha_{Sol}$ = 20 x 10 x 0,10=
$A_{tot} = A_{mur}+A_{plafond}+A_{sol}$ =

$S_{tot} = 2 \times L \times h + 2 \times l \times h + 2 \times L \times l$ = 2 x 20 x 3 + 2 x 10 x 3 + 2 x 10 x 20 = 

$\alpha_{moy} = \frac{A_{tot}}{S_{tot}}$ = a 





