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
Si $\alpha = 1$ : C'est une porte/fenêtre *ouverte* : **Absorption totale**
TR(60) → Tend vers 0
Si $\alpha = 0$ :  **Réflexion totale**
TR(60) → Très grand 

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

## Traitement d'une surface 
Il y a la surface d'avant et celle après traitement. Objectif, enlever l'ancienne surface pour ajouter la nouvelle. 
#### Avant $S_{old}$
On a donc la surface : $A_{old} = \alpha_{old} x S_{old}$ 
#### Après 
On ajoute une nouvelle surface ce qui va nous donner un $S_{new}$ et un $\alpha_{new}$ 
Donc durant la phase de traitement on élimine la surface qui va être remplacer ce qui nous donne un $S_{traitée}$ 
Et on rajoute la nouvelle surface : **$\boxed{A_{new}=A_{old}-\alpha_{old}.S_{traitée}+\alpha_{new}.S_{traitée}}$**  
Ou $\boxed{A_{new}=A_{old}-S_{traitée}.[\alpha_{old}.\alpha_{new}]}$  

## Temps de réverbération : TR(60)
Il est exprimé en seconde. 
### Définition 
La réverbération est la persistance du son dans une salle après l'extinction de la source. Elle est due aux très nombreuses réflexions des ondes sonores. 

![[IMG_0059.jpeg|500]]

### Formule de Sabine
On estime que le silence est revenu lorsque l'énergie sonore est un million(1.10^6) que la perturbation sonore qui a rompu ce silence. 

En effet :
- soit $E_{0}$ l'énergie sonore de la perturbation qui a rompu le silence.
- Soit $E_{1}$ l'énergie sonore mesurée lorsqu'on estime que le silence est revenu telle que $E_1=\frac{E_0}{10^6}$ 
Le niveau sonore résultant est de l'ordre : 

Donc $\boxed{L_1=L_0-60dB}$

>[!note]
>**Attention**, -60dB c'est pas absolue, il faut toujours préférer la division par $10^6$, car si $E_0 = 40dB$ il est physiquement impossible que $E_1 = -20dB$

#### Théoriquement
Le temps de réverbération prévisionnel peut être calculé par différentes formules dont la plus simple reste la formule de Sabine 

Pour établir la formule de Sabine, on va admettre les deux lois expérimentales suivantes : 
- **En tout point de la salle, le niveau énergétique est le même**
- **La variation de l'énergie est proportionnelle à l'énergie instantanée.**

Le temps de réverbération d'une salle est : 
$\boxed{TR_{60}=0,161.(\frac{V}{\alpha_{moy}.S_{tot}})}$  Ou $\boxed{TR_{60}=0,161.(\frac{V}{A_{moy}})}$

Avec $V$ = le volume de la pièce

### Limites de la formule de Sabine 
On sait que (0≤$\alpha_{moy}$≤1)
#### 1er cas
Si $\alpha_{moy} \longrightarrow$ (tend vers) 0 (salle très réverbérante), alors le $TR_{60}$ sera très grand. 
**Vérification** : Soit $TR_{60} = 0,161 . \frac{V}{\alpha_{moy}.S_{moy}}$ alors quand $\alpha_{moy} \longrightarrow$ 0, alors $TR_{60} = 0,161.\frac{V}{0}$ Donc $TR_{60} \longrightarrow + \infty$ (très grand) 
#### 2ème cas
Si $\alpha_{moy} \longrightarrow$  1 (salle très absorbante), alors le $TR_{60}$ doit tendre vers 0 
**Vérification** : Soit $TR_{60} = 0,161 . \frac{V}{\alpha_{moy}.S_{moy}}$ si $\alpha_{moy} \longrightarrow 1$ alors $TR_{60} = 0,161 . \frac{V}{S_{moy}}$ ≠ 0 
C'est donc le défaut de la formule de Sabine, elle ne marche pas pour les matériaux très absorbants. 
#### Conclusion
La formule de Sabine n'est valable que pour des salles peu absorbantes ($\alpha_{moy}<0$) présentant un grand nombre de réflexion. 
Pour les salles plus absorbantes ($0,3<\alpha_{moy}<1$), il est préférable d'utiliser la formule de d'EYRING ou de la formule de MILLINGTON pour calculer le $TR_{60}$. Pour savoir quelle formule utiliser, on commence par sabine et on voit en fonction des résultats si on doit utiliser une autre formule. 
#### EYRING
$$\boxed{TR_{60}=\frac{-0,161.V}{S.ln(1-\alpha)}}$$
#### MILLINGTON 
$$\boxed{TR_{60}=\frac{-4.V}{\sum_{i=1}^{n}[S_i.ln(1-\alpha_l)]}}$$

