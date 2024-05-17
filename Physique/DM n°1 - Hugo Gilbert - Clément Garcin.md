---
aliases: 
Matière:
  - Physique
Semestre:
  - B2-2
Date: 2024-02-27
Prof: Jean Claude Rakotoniaina
Type: Devoir maison
tags:
  - cours
  - Devoir
---
# DM n°1 - Hugo Gilbert - Clément Garcin 
Date: [[2024-02-27]] 

## Étude d'une salle de conférence 
### 1. Intensité et Niveau entendu à 2m 
$I_{2m}=\frac{P_{orateur}}{4\pi.d^2}$ Avec $d=2m$ et $P_{orateur}=12\micro W$ 
$= \frac{12.10^{-6}}{4\pi.2^2}=2,39.10^{-7}\;W.m^{-2}$ 
On va pouvoir calculer le niveau $L_{2m}$ à partir de $I_{2m}$. 
$L_{2m}=10.log(\frac{I_{2m}}{I_{ref}})$ avec $I_{ref} = 10^{-12}\; W.m^{-2}$
$=10.log(\frac{2,39.10^{-7}}{10^{-12}}) = 53,8dB_{SPL}$ 
Le niveau perçu par l'auditeur se trouvant à 2m est dont de $53,8\;dB_{SPL}$ 
### 2. Niveau perçu à 10m
$L_{10m}=L_{2m}-20log(\frac{10m}{2m}) = 39,8\;dB_{SPL}$ 
Le niveau perçu à 10m sera donc de $39,8dB_{SPL}$. Ce qui est vraiment très faible pour de l'écoute continue. Je pense que l'orateur n'a pas été formé au discours devant audience. 
### 3. Niveau Ambiant 
On remarque que $L_{Ambiant} = 70 dB$ est bien supérieur au niveau $L_{orateur}$ perçu par les spectateurs peut importe leur position dans la salle. Donc pour les derniers rangs comme pour les premiers il est nécessaire avec un tel bruit ambiant de sonoriser notre orateur afin que le public puisse apprécier son discours. 
### 4. Niveau Sonore suffisant 
Si le niveau sonore reçu est de $90dB_{SPL}$ alors il sera supérieur au bruit ambiant de 20dB est c'est ce qu'on cherche à obtenir comme résultat

En effet 90-70 = 20dB

### 5. Niveau de l'enceinte à 1m dans l'axe 
On cherche  $L_{1m}$  tel que $L_{5,6m} = 90dB_{SPL}$ 

Donc $L_{1m} = L_{5,6m} - 20 log (\frac{1}{5,6}) = 105 dB_{SPL}$ 

### 6.  Sensibilité
La sensibilité de l'enceinte est de $94dB.w^{-1}.m^{-1}$ (Donc si on lui transmet 1W de puissance le niveau sonore à 1m sera de 94dB)
Donc on cherche $W_{client}$ tel que $L_{client} = 105dB_{SPL}$  :

$L_{client} = Sensibilité + 10.log(\frac{W_{elec(client)}}{W_{elec{usine}}})\Leftrightarrow 105 = 94+10.log(\frac{W_{elec(client)}}{1})$
$\Leftrightarrow 11 = 10.log(W_{elec(client)})$
$\Leftrightarrow 1,1 = log(W_{elec(client)})$
$\Leftrightarrow W_{elec(client)} = 10^{1,1} = 12,6 W$
Il faudra donc fournir 12,6W à l'enceinte pour quelle fonctionne au niveau souhaité. 

### 7. Niveau sonore de l'enceinte capté par le microphone
Pour calculer le niveau reçu par le micro Je vais d'abord calculer le niveaux à deux mètres, puis soustraire l'atténuation du niveau sonore induite par l'angle de 60°. 
$L_{2m} = L_{1m} - 20.log(\frac{2}{1}) = 105 - 6 = 99db_{SPL}$ 
(On aurait pu aussi considérer que come cela double la distance par rapport à l'émetteur on peut retirer 6dB)
Ainsi en ajoutant l'atténuation liée à l'angle on obtient : 
$L_{2m,60°} = L_{2m} - 9 = 99 - 9 = 90dB_{SPL}$ 

### 8. Distance de l'orateur pour éviter les Larsens
Je vais d'abord chercher $I_{enceinte}$ et ensuite utiliser une égalité afin de savoir la distance à laquelle l'orateur transmet au microphone le même niveau que l'enceinte. Il faudra donc qu'il se situe à une distance inférieur car plus $d$ est petit, plus l'intensité est grande. 10^{-12}

$L_{2m,60°} = 90 = 10.log(\frac{\frac{P_{orateur}}{4\pi.d^2}}{I_{ref}})\Leftrightarrow 9 = log(\frac{\frac{P_{orateur}}{4\pi.d^2}}{10^{-12}})\Leftrightarrow 10^9 = \frac{\frac{P_{orateur}}{4\pi.d^2}}{10^{-12}}\Leftrightarrow 10^9.d^2=\frac{\frac{P_{orateur}}{4\pi}}{10^{-12}}$ 
$\Leftrightarrow d = \sqrt{\frac{\frac{P_{orateur}}{4\pi.10^9}}{10^{-12}}}$ 
On a donc d = 0,031 m = 31 cm
L'orateur devra se trouver à maximum 31cm du micro. 
### Question 9
#### 1. Indice de directivité et Q
Le facteur Q est le facteur de directivité de l'enceinte, il permet de savoir si une enceinte est directive ou omni directionnelle. D'après la documentation, le Q de l'enceinte Nexo est de : Q=10
Il est lié à l'indice de directivité (ID) par cette relation : $\boxed{ID=10.log(Q)}$ 
#### 2. Calcul de l'Aire Équivalente d'absorption
Le A représente l'Aire d'Absorption Équivalente. C'est le résultat de la multiplication de d'une surface par son coefficient d'absorption $\alpha$ . Son unité est en $m^2$ (c'est une surface)

Afin de faciliter le calcul je vais représenter mes résultats sous la forme d'un tableau 

|              | Surface (m^2) | Coefficient d'absorption | Aire equivalente |
| ------------ | ------------- | ------------------------ | ---------------- |
| Murs         | 105           | 0,04                     | 4,2              |
| Sol          | 96            | 0,12                     | 11,52            |
| Plafond      | 96            | 0,75                     | 72               |
| Baie vitrées | 15            | 0,03                     | 0,45             |
| Total        | 312           |                          | 88,17            |

Donc $A  = 88,17m^2$

#### 3. Calcul de Q et $r_c$
On a ID = 10dB 
Or comme il y a une atténuation de 9dB à 60° on obtient : 
$ID_{60} = 10 - 9 = 1dB$ 
Ce qui va nous permettre de calculer le Q 
$ID_{60} = 10.log(Q)\Leftrightarrow \frac{1}{10} = log(Q) \Leftrightarrow Q = 10^{\frac{1}{10}}=1,25$

Ce qui nous permet de calculer $r_c$ : 
$r_c=\sqrt{\frac{A.Q}{16\pi}}\Leftrightarrow r_c=\sqrt{\frac{88,17.1,25}{16\pi}}=1,48m$
#### 4. Distance critique
On a trouvé précédemment que la distance critique $r_c$ était égale à 1,5m, or le micro se trouvant à 2m de l'enceinte il capte principalement le niveau réverbéré plutôt que le direct. (1,5m<2m). 
#### 5. Niveau de champ réverbéré 
On sait que $L_{1m} = 105dB_{SPL}$ et $L_{1m,60°} = 105-9 = 96 dB_{SPL}$ 
Donc $L_{1,5m;60°} = L_{1m;60°} - 20.log(1,5) = 92,5dB_{SPL}$ 

Hors à 1,5m soit la distance critique, le niveau direct est égal au niveau réverbéré donc $L_{1,5m;60°} = L_{rev} = 92,5 dB_{SPL}$ 

#### 6. Risque de Larsen 

Il y a un risque de Larsen car le niveau du champ réverbéré est plus important que celui de l'enceinte : $L_{2m;60°} = 90dB_{SPL} < L_{rev} = 92,5dB_{SPL}$ 

La distance à laquelle doit se tenir l'orateur doit donc être différente : 

$d_2 = \sqrt{\frac{\frac{12.10^{-6}}{4\pi.10^{9,25}}}{10^{-12}}}$ = 0,023 m = 23 cm (J'ai remplacé $10^9$ par $10^{9,25}$ d'après les résultats trouvés à la question 8).

Donc il y a un écart de 8 cm par rapport à la question 7 donc si l'orateur c'était mis à la position que l'on avait prévu soit à 31 cm alors il est normal qu'il y ait eu un Larsen à cause du champ réverbéré. Ou du moins le risque est important. 

Après il me semble particulier de développer un tel niveau sonore pour une simple conférence avec 24 personnes. Si le bruit ambiant est de 70dB je pense que les baies vitrées étaient ouvertes est qu'il y avait des travaux à côté ou une route bruyante. Je conseillerais aux propriétaires d'investir dans de l'isolation acoustique pour pouvoir travailler à un niveau plus faible et donc limiter le risque de Larsen dans les futures conférences. 

#### 7. Capsule du microphone 

D'après les diagrammes la capsule avec le plus d'atténuation à 90° (car les enceintes sont perpendiculaires au micro) est la capsule SUPERCARDIOD. De plus le seul risque serait le lobe arrière notamment si on avait du mettre une enceinte de retour pour l'orateur il faudra faire attention à bien ne pas la placer en face du micro pour éviter les larsens. 

