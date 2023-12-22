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
- La puissance de sortie en Watt RMS (Moyenne ou efficace) ou Watt crête (instantanée, environ 2x$W_{RMS}$) 
- Le type d'alimentation (Transfo ou "à découpage")
- La Classe (A, B , AB, D…) (Type de circuit de transistors)
- Le nombres de canaux audio (2 ou plus)
## Caractéristiques
### Sensibilité
La sensibilité indique le niveau électrique du signal audio à l'entrée de l'ampli permettant d'obtenir la puissance max en sortie. En général entre 0 et +6dBu (0,775V et 1,5V). On peut la sélectionner sur certains amplis.
### Puissance de sortie 
- $W_{RMS}$ = Puissance efficace (moyenne), rms = Root Mean Square (racine carrée)
- $W_{crête}$ =Puissance Instantanée (= 2 x $W_{RMS}$)
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
- **Entrée** : 10k$\Omega$ au minimum (pour recevoir des niveaux "lignes" de 1k$\Omega$)
- **Sortie** : < 0,1$\Omega$ car impédance HP environ 8$\Omega$ (avec des *variations en fonction de la fréquence*)

L'impédance est présente dans les caractéristiques (souvent dans le tableau de puissance, si les valeurs ne sont pas présente alors l'ampli ne peut pas supporter ce nombre d'enceinte.) 
#### Important : Montage Série et Parallèle
**SERIE** : Légère perte en puissance, pas de problème d'impédance pour l'ampli. 
$$\boxed{Z=Z_1+Z_2+Z_3}$$ Pour trois enceintes montées en série. Exemple $Z_{1,2,3}$ = 8$\Omega$ on a $Z_{total}$ = 24$\Omega$

**PARALÈLLE** : Augmentation de la puissance mais baisse de l'impédance vue par l'ampli = danger surchauffe. Un ampli peut supporter 8, 4 ou 2$\Omega$ de charge en général, cette valeur dérermine le nombre d'enceintes que l'on peut brancher en paralèlle sur une sortie d'ampli. $$\boxed{\frac{1}{Z}=\frac{1}{Z_1}+\frac{1}{Z_2}+\frac{1}{Z_3}}$$ Pour trois enceintes montées en parallèle. Exemple $Z_{1,2,3}= 8\Omega$ on a $\frac{1}{Z_{total}}=\frac{3}{8}\Rightarrow Z_{total}=2,66\Omega$ 