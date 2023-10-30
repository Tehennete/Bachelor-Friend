---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-26
Prof: David Laurent
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Liaisons HF
Date: [[2023-10-26]] 

>[!NOTE]
>Étude des ondes radio permettant le transport de signaux audio sans fil et de la technologie des émetteurs / récepteurs hf.

## Théorie 
### Introduction
Les liaisons HF sont assez répandues dans divers domaines comme le cinéma, la télévision, la radio, le théâtre, les concerts et autres évènements culturels et sportifs. Ces liaisons sans fil permettent une liberté de mouvements et déplacements ainsi que de limiter l'utilisation de câbles. Elles sont principalement utilisées pour les micros et les retours "oreillettes" (IEM), mais on peut aussi les utiliser entre deux appareils (ex : Mixette / caméra). Ce sont les liaisons que l'on rend sans fil. 
Pour le début à regarder sur internet. 
Le principe est d'utiliser une onde électromagnétique (= composante électrique + Composante magnétique) q'on appellera porteuse (ang = carrier) et qui sera modulée par le signal audio qui sera transporté par celle-ci. 
La porteuse va être modulé et c'est les variations du signal audio qui vont crée la porteuse qui une fois réceptionnée, elle sera démodulée pour retrouve le signal d'origine.

Ci-dessous c'est les différentes variations que l'on peut appliquer à une onde porteuse. 

![[IMG_0039.jpeg|300]] 
Ou soit la porteuse va voir son amplitude varier. Soit la fréquence va varier mais son amplitude restera constante. Soit avec l'inversion de Phase (pas présent sur le schéma).

D'où le nom de radio FM → Frequency Modulation alors que AM signifie Amplitude Modulation.

**Quelques Dates :**
- Le 13 novembre 1886, Hertz réalise la première transmission par faisceau Hertzien entre un émetteur et un récepteur. Ces résultats ouvrent la voie à la télégraphie sans fil et à la radiophonie. 
- Le 12 décembre 1901, le physicien Gugliemo Marconi transmet le premier message en morse transatlantique. Le signal traverse une distance de plus de 3000km au dessus de l'océan.
- Le 24 décembre 1921, la station Tour Eiffel émet la première émission française de radio. Elle dure une demi-heure…
- Le 26 Avril 1935, la première émission de télévision française est émise depuis le ministère des affaires étrangères.
- Le 4 octobre 1960, le premier satellite de télécommunications est lancé par la NASA.
- À compléter avec les premiers appareils professionnels. 
### Comparaison
**Ondes électromagnétique** 
![[IMG_0041.png|400]]
**Ondes Acoustiques**
![[IMG_0042.png]]
**Tableau Comparatif**

|                                                        | Ondes Acoustiques                                                                      | Ondes Électromagnétiques                                                                                                                                                |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nature                                                 | Onde mécanique                                                                         | composante électrique et composante magnétique                                                                                                                          |
| Milieu de propagation                                  | Nécéssité d'un milieu élastique (air, eau, métal, bois) Ne se propage pas dans le vide | Propagation dans tous les milieux y compris le vid                                                                                                                      |
| Type de propagation                                    | Longitudinale (type ressort)                                                           | Transversale(type corde vibrante). La variation des champs magnétique et électriques est perpendiculaire au déplacement de l'onde. Attention au placement des antennes. |
| Vitesse                                                | 340$m.s^{-1}$                                                                          | 300 000 $km.s^{-1}$ (vitesse de la lumière)                                                                                                                             |
| Fréquence (F)                                          | F : 20 Hz – – – 20kHz                                                                  | F : 3Hz — – – $3.10^{20}$Hz • $\lambda$ : 100 000 km – – – 10pm                                                                                                         |
| Longueur d'onde ($\lambda$) (Rappel : $\lambda$ = C/F) | $\lambda$ : 17m – – – 17mm                                                             | $\lambda$ : 17m – – – 17mm                                                                                                                                              |
### Bandes et canaux 
- canal : zone étroite et délimitée contenant un certain nombre de fréquences. 
- Bande : zone étendue et délimitée contenant plusieurs canaux. 
**Vue d'ensemble des ondes électromagnétiques :** 

>[!WARNING] 
>La TNT (télévision numérique terrestre) est sur la même bande que celle des liaisons HFs. Et les canaux de la TNT varient d'une ville à l'autre. Il y a des site qui permettent d'identifier les canaux utilisés par la ville. 

**Détail de la bande UHF (ultra hautes fréquences)**

> [!NOTE]
> Les liaison HF sont autorisée entre 470 et 694 MHz (canal 21 à 48)
> 
#### Remarque 1 
Sous Bandes IV et V situées dans la bandes UHF
	- Sous bande IV : 470MHz - 613MHz (canal 21 à 38)
	- Sous bande V : 613MHz - 862MHz (canal 39 à canal 69)

- 1 canal représente 8MHz de largeur
#### Remarque 2
Les utilisateurs de ces liaisons sont appelés PMSE (Program Making and Special Events) = Tv , théâtre, opéra, concert, évènements médiatiques / culturels / sportifs…

### Modulation FM
On utilise une onde électromagnétique (=PORTEUSE) qui sera modulée en fréquence par le signal audio à transmettre. Plus le signal audio est fort, plus la porteuse s'éloigne de son signal d'origine. La porteuse oscille entre différentes fréquences, elle se balance, elle swing quoi. 
La porteuses suis les variations du signal audio. 
Plus c'est fort plus elle s'écarte beaucoup, inversement si le signal est faible. 
Plus c'est rapide plus c'est la fréquence de variation qui varie en fonction de la fréquence du signal. 

![[IMG_0043.png|300]]

- Nécessite un émetteur (TX), un récepteur (RX) et une porteuse 
- Longueur d'antenne raisonnable (au bout du micro)
- Bande passante audio : 20Hz - 20kHz 
- Dynamique : 120dB environ
- Swing = excursion en fréquence de la porteuse (plus le niveau du signal audio est élevé, plus la porteuse s'écarte de sa valeur d'origine). Le swing est règlementé à 150kHz autour de la porteuse en radio FM et à 56kHz pour les liaisons HF. Ainsi pour respecter la règlementation, les constructeurs placent un limiter audio dans les émetteurs pour que la porteuse respecte son swing
	- Par exemple, si ma porteuse est à 9OMHz elle pourra osciller entre 89,925MHZ ← 90MHz → 90,075MHz
- **Important** : Le signal de la porteuse est noté RF, le signal audio est noté AF. 

>[!note]
> Régler le gain sur le micro, (sur l'émetteur) sur les HF est la chose la plus importante pour que la porteuse module bien (ni trop ni pas assez). Le limiteur, écrête et génère de la distorsion donc on veut l'éviter au maximum. 

C'est ce qui est compliqué, car le gain se fait sur le micro. 

Problème sur les anciens micros HF Shure ou le gain était pas géra le (gain important de base) et donc pour du hip-hop on rentrait dans le limiteur. 
