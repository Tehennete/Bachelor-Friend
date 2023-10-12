---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-11
Prof: David Laurent
Type: notes de cours
---
# Codages des signaux
Dates: [[500 journal/2023-10-12|2023-10-12]]  | Tags : #cours #Technologie-des-équipements

# Codages des signaux
### 1 Codage NRZ

#### Non Return to Zero

La méthode NRZ (Non Return to Zero) représente la technique la plus simle de codage. Dans cette technique à 2 niveaux, le signal numérique est codé suivant les règles : 

- Bit de données à 0 -> tension négative
    
- bit de données à 1 -> tension positive
    

![Le codage NRZ](http://workig.free.fr/image/codage/NRZ.png)

Le codage NRZ

Les principales caractéristiques du codage NRZ sont : 

- Une bonne résistance au bruit
    
- Un mauvaise adaptation au support (spectre centré sur la fréquence nulle)
    
- Peu de transitions, donc difficulté de synchronisation d'horloge
    

### 2 Codage NRZI

#### Non Return to Zero Inverted

Ici, le signal est codé suivant les règles suivantes : 

- bit de donnée à 0 -> la tension s'inverse à chaque période
    
- bit de donnée à 1 -> la tension reste constante à chaque période
    

L'allure de ce signal est représenté ci-dessous : 

![Le codage NRZI](http://workig.free.fr/image/codage/NRZI.png)

Le codage NRZI

L'avantage essentiel de ce codage par rapport au précédent se manifeste dans les transmissions où le signal reste de longues périodes à 0. Dans ce cas, il y a injection de transitions qui facilitent la synchronisation de l'horloge du récepteur.

### 3 Codage Manchester

Une solution permettant de décaler le spectre du signal vers les fréquences plus élevées consiste à coder les états de base par des transitions et non par des niveaux. C'est la solution adoptée par le codage Manchester, encore appelé _codage biphase_.

Cela se traduit par les règles suivantes :

- bit de donnée à 0 -> un front montant
    
- bit de donnée à 1 -> un front descendant
    

L'allure de ce signal est réprésenté ci-dessous :

![Le codage Manchester](http://workig.free.fr/image/codage/manchester.png)

Le codage Manchester

Caractéristiques de ce codage : 

- Bonne résistance au bruit (2 niveaux)
    
- Bonne adaptation aux supports à bande passante large
    
- Beaucoup de transitions, donc facilité de synchronisation d'horloge
    

Le principal inconvénient de ce code réside dans la grande largeur de son spectre, ce qui le confine aux supports à large bande comme les câbles coaxiaux

### 4 Codage Manchester Différentiel

Cette variante du codage de Manchester correspond aux règles suivantes : 

- écart entre donnée i et i-1 égal à 0 -> front montant
    
- écart entre donnée i et i-1 égal à 1 -> front descendant
    

Les caractéristiques de ce code se trouvent sur le schéma suivant : 

![Le codage Manchester différentiel](http://workig.free.fr/image/codage/manchesterdifferentiel.png)

Le codage Manchester différentiel

### 5 Code de Miller

Le code de Miller s'obtient à partir du codage Manchester dans lequel on supprime une transition sur deux. En d'autres termes, les règles d'encodages prennent la forme suivante : 

- Si le bit de donnée vaut 1, alors on insère une transition au milieu de l'intervalle significatif
    
- Si le bit de donnée vaut 0, alors pas de transition au milieu de l'intervalle significatif, mais si le bit suivant vaut 0, alors on place une transition à la fin de l'intervalle significatif
    

L'exemple suivant illustre le codage de Miller :

![Le codage de Miller](http://workig.free.fr/image/codage/Miller.png)

Le codage de Miller

Les caractéristiques de ce code sont les suivantes : 

- permet des débits élevés sur support à bande passante limitée
    
- Une puissance non nulle est transmise pour la fréquence nulle, ce qui peut introduire des distorsions
    

Le principal inconvénient de ce code tient en une moins grande immunité vis-à-vis du bruit que les codes précédents.

### 6 Codes bipolaires

Les codes à 3 niveaux se distinguent par un spectre à bande étroite qui possède en outre la propriété de s'annuler quand la fréquence tend vers 0.

Nous nous limiterons à la description du codage bipolaire simple

Le signal bipolaire comporte 3 niveaux : 

- -a
    
- 0
    
- +a
    

La loi de codage se caractérise par les règles suivantes :

- Si le bit de donnée est à 0 alors le niveau résultant est nul
    
- Si le bit de donnée est à 1, alors le niveau est alternativement égal à -a et à +a
    

![Le codage bipolaire simple](http://workig.free.fr/image/codage/bipolairesimple.png)

Le codage bipolaire simple

### 7 Choix d'un type de code

|   |   |
|---|---|
|![[Important]](http://workig.free.fr/images/important.png)|Important|
|Attention ce qui suit dans cet encadré est _hors programme_. Cela n'a été placé ici que pour votre information afin que vous compreniez l'origine de la décision de l'utilisation d'un codage plutôt qu'un autre. Tout ceci pour vous dire que ça n'est en rien empirique, mais que cela repose bien sur une base scientifique.<br><br>Le spectre en puissance exprime la caractéristique fondamentale du signal (NRZ, NRZI, Miller etc.) Son calcul sort du niveau fixé pour ce cours. Afin de vous donner un aperçu, voici quelques équations finales pour les codages que nous venons d'étudier : <br><br>- _NRZ_ : <br>    <br>    - _Répartition de puissance (densité spectrale) en fonction de la fréquence f_<br>        <br>        ![](http://workig.free.fr/image/codage/eq_NRZ.png)<br>        <br>    - _largeur à mi-hauteur du spectre en puissance_<br>        <br>        ![](http://workig.free.fr/image/codage/eq_NRZ02.png)<br>        <br>    <br>- _NRZI_|

L'objectif essentiel consiste à adapter le signal au support de transmission. Les différents codes, excepté le NRZ, introduisent de la redondance (d'une grande fréquence du nombre de transitions pour le Manchester ou de niveau pour le bipolaire). 

Le code NRZ est le moins sensible aux erreurs. Le spectre du code Manchester admet 2 fois plus de bruit que le code NRZ, car sa caractéristique est deux fois plus large. Celui du bipolaire est également plus sensible au bruit puisqu'il possède plus de niveaux. Enfin, le code de Miller qui possède une puissance non nulle à fréquence nulle présente une tolérance réduite vis-à-vis du bruit.

![spectres des différents modes de codage en bande de base](http://workig.free.fr/image/codage/spectre.gif)

spectres des différents modes de codage en bande de base

---
