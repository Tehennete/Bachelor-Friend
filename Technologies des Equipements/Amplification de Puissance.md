---
aliases: 
Matière:
  - Technologie des Equipements
Semestre:
  - B2-1
Date: 2023-12-20
Prof: "[[David Laurent]]"
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Amplification de Puissance
Date: [[2023-12-20]] 
### Objectif 
## Introduction
### Rôle 
Il sert à amplifier des signaux de niveau ligne (+4dBu) pour les amener à quelques dizaines de Volts et plusieurs Ampères ainsi qu'une faible impédance de sortie afin de sortir la puissance nécessaire et d'assurer le bon fonctionnement des haut-parleurs
### Principe
- Basé sur l'utilisation des transistors de puissance de type FET (Field Effect Transistor) ou de MOSFET (Métal Oxyde Silicium FET) qui assurent l'élévation de la tension électrique en sortie. Ces composants nécéssitent une alimentation électrique importante réalisée par des transfos (bobines + pont de diodes) ou des circuits appelés "à découpage"

La classe d'un ampli ça correspond à l'ajustement du circuit de transistors. 

>[!note] Important !
>Le gain d'un amplificateur est fixe ! En général +26dB ou +32dB, le potentiomètre de réglage "volume" est un atténuateur du signal audio de $-\infty$ à OdB
>

Les transistors ne sont pas variables. C'est un atténuateur qui va baisser le signal que l'ampli reçoit. La première partie du circuit de l'ampli c'est l'atténuateur. On baisse de préférence l'atténuateur de l'ampli car c'est c'est l'élément le plus loin dans la chaîne du son, ce qui permet moins de défauts de rapport signal/bruit. En baissant sur la console, on envoie un signal avec un mauvais signal/bruit. 

Les transistors on des plages de fonctionnement idéales. 

### Modèles 
**Ils diffèrent suivant :**
- La puissance de sortie en Watt RMS (Moyenne ou efficace) ou Watt crête (instantanée, environ 2x $W_{RMS}$) 
- Le type d'alimentation (Transfo ou "à découpage")
- La Classe (A, B , AB, D…) (Type de circuit de transistors)
- Le nombres de canaux audio (2 ou plus)
## Caractéristiques
### Sensibilité
La sensibilité indique le niveau électrique du signal audio à l'entrée de l'ampli permettant d'obtenir la puissance max en sortie. En général entre 0 et +6dBu (0,775V et 1,5V). On peut la sélectionner sur certains amplis.
### Puissance de sortie 
- $W_{RMS}$ = Puissance efficace (moyenne), rms = Root Mean Square (racine carrée)
- $W_{crête}$ =Puissance Instantanée (= 2 x $W_{RMS}$ )
- Rappel formules : $\boxed{P=U.I}$ et $\boxed{U=Z.I}$
### Réponse en fréquence
- Insique la zone de fréquence dans laquelle l'ampli présente un fonctionnement constant (mesure faite à bas niveau, en général 1W sous 8$\Omega$ Standard : 20Hz - 20kHz)
- C'est un des appareils les plus droits en réponse en fréquence. La courbe de fréquence de réponse d'un ampli est droite et n'est pas un critère prioritaire. 
### Distortion THD
- THD : Total Harmonie Distortion
- Comparaison d'un signal d'entrée sinusoïdal pur avec le résultat en sortie à la puissance max de l'ampli 
- En général < 0,05%

>[!Note]
>La **distortion d'intermodulation** est une caractéristique importante. 
>Exemple : On injecte 10kHz et 11kHz et on mesure le niveau de présence du 1kHz (11-10) présent en sortie. Il devrait être < de 70dB environ du niveau d'entrée. 

### Diaphonie
= Cross-talk (en anglais)
C'est la présence plus ou moins importante du canal 1 dans le canal 2 par rayonnement électromagnétique de circuit et des câbles à l'intérieur de l'ampli. De plus, le courant "appelé" sur un des canaux peut entraîner une modulation de la tension d'alimentation (transfo) qui se répercute sur l'autre canal 

La valeur donnée est l'atténuation en dB qui doit être la plus grande possible : environ 70dB pour les fréquences médium et 50dB pour les basses fréquences. 

On peut la limiter en utilisant 2 transfos différents dans l'ampli et des condensateurs de filtrage. 

En utilisant deux amplis différents pour chaque signal cela permet d'éviter les problèmes de diaphonie.
### Rapport Signal / Bruit 
C'est le rapport entre la tension max en sortie et le bruit de fond résiduel de l'ampli (mesure effectuée avec l'entrée de l'ampli court-circuitée). 
- En général > 100dB

>[!note]
>Plus l'ampli est puissant, plus le S/N doit être grand afin que le bruit résiduel soit inaudible même à fort volume. 

### Impédance d'entrée et sortie 
- **Entrée** : 10k $\Omega$ au minimum (pour recevoir des niveaux "lignes" de 1k$\Omega$)
- **Sortie** : < 0,1 $\Omega$ car impédance HP environ 8$\Omega$ (avec des *variations en fonction de la fréquence*)

L'impédance est présente dans les caractéristiques (souvent dans le tableau de puissance, si les valeurs ne sont pas présente alors l'ampli ne peut pas supporter ce nombre d'enceinte.) 
#### Important : Montage Série et Parallèle
**SERIE** : Légère perte en puissance, pas de problème d'impédance pour l'ampli. 
$$\boxed{Z=Z_1+Z_2+Z_3}$$ Pour trois enceintes montées en série. Exemple $Z_{1,2,3}$ = 8 $\Omega$ on a $Z_{total}$ = 24 $\Omega$

**PARALÈLLE** : Augmentation de la puissance mais baisse de l'impédance vue par l'ampli = danger surchauffe. Un ampli peut supporter 8, 4 ou 2$\Omega$ de charge en général, cette valeur dérermine le nombre d'enceintes que l'on peut brancher en paralèlle sur une sortie d'ampli. $$\boxed{\frac{1}{Z}=\frac{1}{Z_1}+\frac{1}{Z_2}+\frac{1}{Z_3}}$$ Pour trois enceintes montées en parallèle. Exemple $Z_{1,2,3}= 8\Omega$ on a $\frac{1}{Z_{total}}=\frac{3}{8}\Rightarrow Z_{total}=2,66\Omega$ 

### Facteur d'amortissement (Dumping Factor)
C'est une indication de la manière dont l'ampli "commande" les mouvements du HP. En effet les membranes de HP ont tendance à continuer à osciller après que le signal ait cessé. Une impédance de sortie d'ampli très faible court-circuite alors virtuellement le HP ce qui permet d'amortir ces oscillations résiduelles de membrane.
Le facteur d'amortissement est le rapport entre l'impédance de charge du HP et l'impédance de sortie de l'ampli. 
Exemple : facteur 100 avec HP de 8$\Omega$ signifie que l'impédance de sortie de l'ampli sera de 8/100 = 0,08 $\Omega$ 

Plus le facteur est élevé, meilleure sera la liaison ampli-HP, il concerne surtout les basses fréquences pour lesquelles l'excursion de la membrane est importante et doit être contrôlée. 

## Classes d'Ampli

Les classes d'ampli ce sont le type montage d'amplification choisit par le constructeur
### Classe A
- Utilise un seul transistor de puissance (==polarisé==) pour amplifier le signal 
- Faible rendement
- Très bonne qualité audio (Hi-FI haut de gamme)
- Nécéssite un courant de polarisation qui circule en permanence afin d'assurer un fonctionnement linéaire des circuits. Il consomme donc de l'énergie même s'il n'y a pas de signal audio à l'entrée.
### Classe B
- Utilise 2 transistors en mode "Push-pull", l'un amplifie la partie positive du signal audio et l'autre la partie négative. Ensuite on ré-combine les 2 en sortie.
- Rendement important 
- Distorsion présente à faible niveau d'utilisation + distortion au point de raccordement
- Qualité audio moyenne : utilisation qui ne requiert pas de haute fidélité (talkies, Dictaphones, jouets…)
![[Amplification de Puissance 2024-01-11 10.09.42.excalidraw]]
### Classe AB
- modèle très courant 
- Classe A à faible puissance et classe B à forte puissance 
- Bonne qualité audio 

### Autres Classes 
#### Classe C
Amplificateur pour diffusion radio ou [[Liaisons HF]] en Modulation de fréquence (FM) avec antenne (on injecte une bande étroite de fréquences à un circuit résonnant)
#### Classe D
Assez courant, fonctionne par modulation à largeur d'impulsion. Un signal impulsionnel généré par L'ampli module le signal d'entrée (MLI = Modulation à largeur d'impulsion ou PWM = Pulse WIdth Modulation) les impulsions obtenues sont amplifiées puis filtrées en sortie par un pass-bas. On dit que l'ampli fonctionne comme un commutateur. Parfois appelé ampli numérique (À tort). Souvent utilisé pour les ampli de Subwoofer car le rendement est important. Distortion supèrieure à la classe AB

On fabrique des impulsion électriques en fonction du signal audio plus plus le signal est fort plus l'impulsion est large. Et c'est le signale converti qui sera amplifié. En suite on  fait passer le signal à largeur d'impulsion dans un circuit pour restituer le signal audio d'origine mais amplifié. 

![[IMG_0077.jpeg|400]]

À creuser. 
#### Classe i
Méthode spécifique développé par la marque [[Crown-Amplification]], combinaison des classes B et D (Cf doc en annexe)
#### Classe E, F 
Tentatives d'améliorations du rendement 
#### Classe G
Variante de la classe A avec 2 circuits d'alimentation (1 faible et 1 forte en fonction des besoins)


#### Classe H

>[!note]
>Il s'agit d'**un mode d'alimentation des circuits d'amplification** qui consiste à remplacer le transformateur (Bobine + diodes) par des circuits appelé "alimentation à découpage"
>Donc la on ne parle pas du circuit d'amplification mais bien du type d'alimentation de ce circuit 

- Souvent associé à une classe D ou AB
- Avantages : chauffe peu, Poids léger 

## Modes d'utilisation 
C'est selectionnable directement sur l'ampli. Ça ce fait souvent avec un switch.
### Stéréo (ou dual Mono)
- Chaque canal de l'ampli fonctionne de manière indépendante
- C'est le mode d'utilisation standard des amplis
**Schéma stéréo (ou dual-mono)**

### Parallel - Mono
- Un seul canal est disponible en entrée dont la modulation est envoyée dans les 2 canaux d'amplification 
- Utile quand on veut envoyer un meme signal sur plus d'enceintes. (Quand on atteint la limite d'enceinte d'un des canaux de l'ampli.)
**Schéma Parallel mono**

### Bridged (Mono)
- Un seul canal est disponible en entrée **ET** en sortie, donc fonctionnement mono. Par contre, on combine la puissance des deux canaux d'amplification afin d'obtenir une puissance disponible en sortie x3. Il faut se renseigner sur les bornes de sortie de l'ampli à utiliser dans ce mode de fonctionnement particulier. Souvent utilisé en sono pour les Subs. 
**Schéma Bridged-Mono

### Divers
- Protections : 
	- Fusible si court-circuit, contre les variation de tension (220V)
	- limiteur pour protéger les HP
	- mesure de la température intérieure de l'ampli avec coupure audio si nécéssaire….
- Il existe des amplis à 2, 4 8 canaux 
- **La connectique de sortie est en général** :
	- *Speak on (2 ou 4 points)
	- *Bernier à visser*
	- *Fiche banane* 

## Amplificateurs avec Processing (ou Contrôleurs Amplifiés)
On trouve couramment aujourd'hui des amplificateurs auxquels on a ajoutés certaines fonctionnalités et traitement du signal audio. C'est traitements sont réalisés en numérique, on trouve donc un CAN juste après l'entrée analogique de l'ampli ou des entrées directement numériques (ou réseau rj45), puis un bloc de processeur (DSP) en enfin un CNA avant d'entrer dans les circuits de puissance. 

#### Les fonctions principales de ces processeirs sont
- Gain
- Inversion de phase
- EQ
- Retard (Delay)
- Filtre coupe bas ou filtre séparateur (cross-over)
- Routing
- Limiteur 
- Mémoire (Preset) Contenant tous les réglages constructeurs spécifiques pour chaque modèle d'enceinte de la marque qu'on peut utiliser. 
*Exemple* : Ampli 4 Canaux LA8 de [[L-Acoustics]]
