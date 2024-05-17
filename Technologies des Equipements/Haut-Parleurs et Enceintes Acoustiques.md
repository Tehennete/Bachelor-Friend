---
aliases:
Matière:
  - Technologie des Equipements
Semestre:
  - B2-2
Date: 2024-02-01
Prof: "[[David Laurent]]"
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Haut-Parleurs et Enceintes Acoustiques
Date: [[2024-02-01]] - [[2024-04-12]] 

#### Objectif
Étude de la technologie des enceintes acoustiques et de leurs caractéristiques techniques. Les haut-parleurs seront abordés au préalable afin de comprendre la transduction électrique-acoustique. 

## Introduction
- Le Haut parleur est un transducteur électrique-acoustique qui permet de transformer une version de tension électrique en un mouvement mécanique de membrane créant ainsi une variation de la pression acoustique.
- Une enceinte acoustique est une "boite" très souvent en bois à l'intérieur de laquelle sont installés un ou plusieurs Haut-parleurs. 

## Haut-parleurs 
### Haut-parleur électrodynamique (à bobine mobile)
#### Généralité
- C'est le modèle le plus répandu (pro et grand-public)
- le principe technologique est l'inverse de celui étudié pour le micro dynamique (aimant +bobine + membrane). Un courant parcourant un conducteur électrique placé dans le champ magnétique D'un aimant provoque son déplacement. Le sens du déplacement dépend du sens du courant, ainsi un courant alternatif provoquera des mouvements d'oscillation de la membrane en fonction de la fréquence de ce courant. Par ailleurs, plus la tension sera élevée plus le mouvement sera important donc la pression acoustique générée également. 
- 1er brevet : Wermer en 1877, mais pas de puissance électrique pour assurer son fonctionnement. 
- 1er Modèle : Kellog & Rice en 1925 + fabrication d'un ampli 1 Watt. 
#### Principaux éléments constitutifs
- Aimant : en forme de galette perforée au centre (entrefer), qui crée un champ magnétique puissant. 
- Bobine : Solidaire de la membrane, elle est parcourue par le courant issu de l'amplificateur et se met en mouvement car placée dans le champ magnétique de l'aimant. C'est un élément fragile car elle chauffe beaucoup. 
- Membrane : Surface en matériaux cartonneux renforcé par un vernis ou du carbone, elle est mise en mouvement par la bobine et crée la pression acoustique entendue par l'auditeur. 
	- Grande surface : Fréquence basses | Petite surface : Fréquences aigues
	- En se déformant lors du mouvement elle a un effet sur le rendement des hautes fréquences, la courbe de réponse et la directivité (les aigus focalisent au centre). 
- Spider (8 sur le doc) : Suspension de centrage : Permet de d'assurer le centrage de la bobine et a un rôle d'anti poussière. Et assure également le rappel de la membrane c'est la compliance du haut parleur → Cs (c'est une valeur qui intervient dans le calcul de la fréquence de résonance du haut-parleur). ((En général on fait en sorte que cette fréquence soit en dehors du spectre)). 
- La suspension périphérique (3) : Elle sert au centrage de la membrane et de la bobine. Elle sert à amortir les ondes qui se propagent à travers la membrane (comme une plaque en acier qu'on frotte avec un archet), que l'on nomme modes vibratoires. Elle a donc une influence sur la courbe de réponse. 
- Le cache noyau /bobine (1 Ogive au centre de la membrane) : Anti-poussière, il a un role dans la réponse en fréquence des aigus. 
- 

>[!note]
>Quand il y a des impurtée sur un HP, on entend des bruit de frottements/grésillement sur les kick où les basses.  
### Réponse en Fréquence 
- **Indique la zone de fréquence dans laquelle l'ampli présente un fonctionnement constant (mesure faite à bas niveau, en général 1W sous $8\Omega$ . Standard : 20Hz - 20kHz)**
### Distosion (THD)
- THD : Total Harmonic Distotion

### Haut parleur  Electrostatiques 
Principalement dans le monde de la hi-fi
- Beaucoup moins courant 
- Plus de contenue en fréquences 
- Niveau sonore limité (hi-fi)
- Excellente qualité audio 
- Directivité souvent bidirectionnel
- Marque qui utilise beaucoup cette technologie : Martin Logan (Quad ESL63)

### À Ruban
Même principe que pour les micros. 
La bobine et la  membrane sont remplacées par un seul élément : le ruban.
- Plutôt utilisé pour les tweeters (pour reproduire les aigus)
- Marque qui utilise beaucoup les tweeters à Ruban : ADAM 
- Souvent la manière dont ça produit le son, est soit en déplacement soit en pincement entre les différentes faces du rubans. C'est un mouvement d'écrasement. 

### Piezo - Électrique 
#### Céramique 
Ressemble à des disque empilés qui se déforment en épaisseur lorsqu'ils sont soumis à une tension électrique. 
Ces disque sont reliés à une membrane. 
#### Film Plastique
Ça se déforme en élongation cette fois .

Milieu bas de gamme et pour les appareil domestiques qui font du son (jouet, ou appareils ou la qualité audio c'est pas la priorité)

### Autres expérimentations
#### À Plasma
Variante de l'électrostatique mais avec de l'air ionisé. Il n'y a plus de membranes, les particules sont directement mises en mouvement. 
#### Numérique
L'objectif était de rester numérique sur toute la chaîne. 
On fait correspondre chaque valeur binaire, de chaque échantillon, à une surface piezo proportionnelle au poids de chacune 

nom anglais : **Digital speakers** or **digital sound reconstruction** (DSR)

### Note Haut parleur spécialisé dans aigus  
#### A dôme
#### À Cone

## Marques de Haut-parleurs

PHL Plutôt pour les medium
AUDAX aigus

## Enceintes Acoustiques

Pourquoi on met les haut-parleurs dans des boites? 
→ Le rayonnement d'un haut pâleur en champ libre est égal en énergie vers l'avant et l'arrière avec une polarité inversée. 

![[Haut-Parleurs et Enceintes Acoustiques 2024-03-27 09.56.22.excalidraw]]
On va essayer de récupérer cette énergie. 
On place le haut-parleur dans une enceinte de sorte à atténuer l'influence de l'arrriere.

### Enceinte close
On l'onde arrivere va être contrainte par un boîtier 


![[Haut-Parleurs et Enceintes Acoustiques 2024-03-27 10.00.27.excalidraw]]
C'est le modèle mécanique le plus simple.
la qualité de fabrication, le choix du bois, la densité de la mousse vont participer a la qualité de l'enceinte. Il s'agit du modèle le plus simple et le plus courant. 
L'absorbant va limiter la resurgence de l'onde arrière.

C'est pourquoi dans certains studios, les enceintes sont encastrées dans les murs. Ou le le petit résidu arrière est éliminé. On le voit souvent sur les grosses écoutes dans les studios (surtout sur les subs). Il est interessant de le faire sur le dur du mur.
Donc à prévoir en amont.

### Bass-Reflex
Il s'agit d'une enceinte avec un évent.
![[Haut-Parleurs et Enceintes Acoustiques 2024-03-27 10.18.31.excalidraw]]
Ce sont des calculs fait par les concepteurs qui sont fait en fonction du haut-parleurs, de la boite, de l'onde que l'on veut mettre en avant.
Un bass-reflex s'accorde.
Cela permet une remise en phase et une redirection de l'onde arrière grave qui sera augmenté. 
En surexploitant cet effet cela peut transformer un grave plus ventu/soufflant que les graves que peut produire un haut parleur de taille supérieur.

Augmentation dans les basses fréquences par recuperation de l'onde arrière. De nombreuses enceintes fonction ainsi car cela ne coute pas grand chose tout en améliorant les capacités des subs et l'extention de la réponse  en fréquence dans les basses freaquences. 

Regarder si la qualité de matériau du tube a une influence sur la qualité de l'enceinte. 

IK multimedia → correcteur système de correction multimedia → solution hardware. 
Solution logiciel → Sonarworks 

PMC bass-reflex avec une colonne arrière.
### A Labyrinthe / ligne de transmission/pavillon replié

Cela nécessite une enceinte assez profonde pour réaliser le labyrinthe. On va jouer sur le retard. On peut étendre la réponse en fréquence dans le grave en jouant sur la différence de trajet entre avant et arrière. 
![[Haut-Parleurs et Enceintes Acoustiques 2024-03-27 10.59.57.excalidraw|200]]
### Charges "avant"
On va chercher à modifier le caractère avant de l'enceinte. L'objectif sera de diriger et contrôler la directivité horizontale et verticale des enceintes. Pour des utilisation plus précises. En monitoring notamment ou pour des face/retours en façade. 
#### Chambre de compression/moteur à compression 
Cela concerne principalement les tweeter (aigus)
On place une charge à proximité du tweeter de sorte à comprimer l'air devant la membrane permettant ainsi d'augmenter la pression acoustique. On aura une pression acoustique plus élevée malgré la même injection de puissance. L'air est comprimé avec des elements solides qui en réduisant le canal les comprime avant de les libérer.
#### Pavillon 
C'est une pièce mécanique que l'on va placée devant le haut parleur principalement les tweeters. Cela permet de guider, diriger et maitriser la directivité horizontale et verticale de celui-ci dans les aigus. 

>[!note] 
>Il est indispensable de connaître la directivité des enceintes afin de les placer correctement. 

### Enceintes à plusieurs voies 

#### Système 2 voies 
Soit avec un montage coaxiale : un boomer + un tweeter placé  derrière au centre
Le haut-parleur aura donc deux borniers et aura besoin d'être filtré.

→ [[Haut-Parleurs et Enceintes Acoustiques#]]

Soit un montage plus classique avec deux hauts-parleurs séparés : woofer + tweeter également.  

Les deux voies nécéssite un filtrage préalable du signal audio pour chacun des HP à l'aide d'un cross-over. Répartissant le grave et l'aigu dans les deux différents HP (Check filtres RMC)
##### Filtrage 
Objectif donner à chaque haut parleur la bonne zone de fréquence de chaque haut parleur. 

###### Filtrage passif 
Le filtre est **après** l'ampli. Donc le filtre est dans l'enceinte. C'est un filtre séparateur ou cross-over. La fréquence pour une enceinte 2 voies est d'environ 2kHz. Il y a donc une sortie de filtre pour les hautes fréquences et une sortie pour les basses. 

La manière la plus simple c'est un filtre RLC : ![[Haut-Parleurs et Enceintes Acoustiques 2024-04-12 13.15.00.excalidraw]]

###### Filtrage actif
On filtre **avant** l'ampli. L'objectif est d'améliorer le rendement (et la courbe de réponse) 
Le signal audio va entrer dans un filtre et on aura deux sorties audio du filtre que l'on va ensuite amplifier. Donc il faut un circuit à 2 voies. (4 pour de la stéréo)

ON va donc utiliser le speakon 4 points qui a 4 liaisons indépendantes. Qui permettra de repartir les signaux au bon endroit. 
En general la norme utilisé est 1+ 1- 2+ 2-. 1 pour le low et 2 pour le high. 
Donc il faudra un câble HP de 4x2,5m$^2$ 
On l'appel parfois bi-amplification. 

Solution plus coûteuse mais permet une meilleur linéarité. 
Aujourd'hui les amplis ont parfois le filtre directement intégré à l'ampli. 

Cette pratique a généralisé cette pratique avec plus que 2 canaux. 
Et ils ont rajouté des choses petits à petit, comp , eq fx….

>[!Note]
>Certaine enceintes sont équipées de leur amplificateurs. 
>on devrait utiliser le terme d'enceinte auto-amplifiée ou d'enceinte amplifiée. 
>Penser à demander d'éclaircir le terme si on n'est ps sûr. 
>De façon precise on devrait dire : Enceinte amplifiée 2 vois à filtrage passif 

On utilise le terme actif et passif pour designer le fait que l'enceinte est équipée en interne de l'amplification. 

On peut utiliser aussi le terme d'enceinte bi-amplifier. 
##### Remarque : 3 voies 

C'est la meme chose mais avec un filtre avec 2 fréquences de coupes. 

### Les Subwoofers 
Enceintes spécialisée dans la reproduction des très basses fréquences en general en dessous de 100 Hz. 
Dans une configuration multicanal en audio cinema il se nomme le **LFE** = Low Frequency Effect. Il arrive de temps en temps, c'est un effet. 
Il s'agit du .1 des formats en multicanal (5.1 ; 7.1)

Parfois en sono les subs se font uniquement sur un aux ce qui permet de doser le sub en live. On l'utilise alors comme un effet en sono. 

### Caractéristiques 
#### Impédance 
En general c'est $8\Omega$, attention c'est une valeur moyenne. Ce n'est pas $8\Omega$ à toutes les fréquences. Il varie avec la fréquence. 
#### Sensibilité 
Parfois appelée rendement. C'est le nombre de $dB_{SPL}$ à un metre pour 1 Watt. 
Ex : $86dB.W^{-1}@1m$ 
Et on donne aussi le max SPL ce que l'enceinte est capable au maximum avec une distortion minimum. 
#### Distortion 
Elle est présente particulièrement dans les basses fréquences. 
- med/aigu < 1% 
- Basse < 10% 
#### Réponse en fréquence 
Idéalement on aimerait que ce soit plat sur 20Hz - 20kHz 
Ce n'est pas linéaire, donc important de le regarder. 

#### Tenue en puissance 
Nombre de watts supportés avant distortion importante.
Ex : sensi : $86dB.W^{-1}@1m$
Tenue en puissance 30 watt
Donc augmentation de la puissance en dB de 1 à 30w → $10.log(\frac{30}{1})=15dB$ 
Donc niveau max = 86 + 15 = $101dB_{SPL}$ $86dB.W^{-1}@1m$ 
#### Directivité 
Horizontale en dégrées
Verticale en dégrées 

Ce sont des valeurs moyennes, pour plus de précision il faut aller voir le diagramme de directivités qui permet de connaître les directivités à toutes les fréquences. 

>[!note]
>Système line-array = ensemble d'enceintes superposées dont la directivité verticale est de quelques degrés et la directivité horizontale d'environ 100degré 
→ on définit la directivité verticale par le nombre d'enceinte et les angles entre chacune.
On les cale avec des plans puis au laser. 




#### Type de haut parleur 
On donnera les différents types de HP utilisés. 
