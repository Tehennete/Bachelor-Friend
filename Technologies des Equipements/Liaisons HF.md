---
Matière:
  - Technologie des Equipements
Semestre:
  - B2-1
Date: 2023-10-26
Prof: "[[David Laurent]]"
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Liaisons HF
Date: [[2023-10-26]] - [[2023-11-29]] - [[2023-12-01]] - [[2023-12-06]] 

>[!NOTE]
>Étude des ondes radio permettant le transport de signaux audio sans fil et de la technologie des émetteurs / récepteurs hf.

## Théorie 
### Introduction
Les liaisons HF sont assez répandues dans divers domaines comme le cinéma, la télévision, la radio, le théâtre, les concerts et autres évènements culturels et sportifs. Ces liaisons sans fil permettent une liberté de mouvements et déplacements ainsi que de limiter l'utilisation de câbles. Elles sont principalement utilisées pour les micros et les retours "oreillettes" (IEM), mais on peut aussi les utiliser entre deux appareils (ex : Mixette / caméra). Ce sont les liaisons que l'on rend sans fil. 
Elles seront découvertes à la fin du XIXème siècle.
Le principe est d'utiliser une onde électromagnétique (= composante électrique + Composante magnétique) q'on appellera porteuse (ang = carrier) et qui sera modulée par le signal audio qui sera transporté par celle-ci. 
La porteuse va être modulé et c'est les variations du signal audio qui vont moduler la porteuse qui une fois réceptionnée, elle sera démodulée pour retrouve le signal d'origine.

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
| Fréquence (F)                                          | F : 20 Hz – – – 20kHz                                                                 | F : 3Hz — – – $3.10^{20}$                                                                                                         |
| Longueur d'onde ($\lambda$) (Rappel : $\lambda$ = C/F) | $\lambda$ : 17m – – – 17mm                                                             | $\lambda$ : 100 000km – – – 10pm                                                                                                                                               |
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

Problème sur les anciens micros HF Shure ou le gain était pas gérable le (gain important de base) et donc pour du hip-hop on rentrait dans le limiteur. 
## Technologie 
### Antenne 
#### Généralités
- Une antenne assure la transformation d'un signal électrique qui la parcourt en ondes électromagnétique et inversement (une même antenne peut donc être utilisée dans certains cas pour émettre et dans d'autres pour recevoir)
- La directivité s'exprime par : le gain de l'antenne en dBi (calculé par rapport à une antenne isotrope = sphère parfaite) donc on donnera jamais de directivité mais simplement la valeur en dBi pour avoir la directivité. Il y a une plage de fréquence dans laquelle, elle est efficace. 
- QUand on perd -3dB de capitation par rapport à l'axe de par et d'autre de son axe cela donne son angle d'ouverture par rapport à sa direction privilégiée. 
- Le rendement est faible (quelques %), pour augmenter on essaye d'utiliser des longueurs d'antennes proches des longueurs d'ondes des porteuses (ou1/2, ou ¼). On appelle cela l'accord de l'antenne.

>[!note]
>Pour F = 600MHz on a $\lambda$ = 50 cm

- Le placement idéal des antennes : à vue (que émettrice et la réceptrice puissent se voir), en hauteur et parallèles (même sens de polarisation)
- quand on a deux antennes dans un boîtier en rack, on va mettre les antennes à 90° l'une de l'autre afin que le boîtier puisse choisir l'antenne qui est la plus efficace, si on les met en parallèles, c'est comme si il n'y en avait qu'une car les deux couvrent et captent la même chose. 
#### Modèles
##### Doublet (ou dipôle)
- accordée en ½ $\lambda$ 
- L environ 25 cm
- Omnidirectionnelle (l'omni d'une antenne à une forme de donut/torus) 
##### Antenne libre (antenne "fouet")
- accordée en ¼ $\lambda$ (ou parfois ½ $\lambda$) / semi-omnidirectionnelle / Bande passante étroite.
Elle fonctionne comme un omni mais comme on a pas les deux côté comme dans l'antenne doublet, et que l'une des bornes soit reliée à la masse de l'appareil. Alors le donut de l'omni est bloqué et donc coupé en deux par le plan de masse. 
- L environ 12 cm
- Très utilisée sur les récepteurs (et émetteurs parfois)
##### Yagi
- inventée en 1930 par un ingénieur Japonais
- Antenne très directive souvent utilisé pour la reception télé chez les particuliers
- La première barre sert de réflecteur qui va empêcher les ondes d'arriver sur l'antenne qui est la deuxième barre 
- Les petites barres après vont diriger le signal vers l'antenne qui vont accentuer la directivité. 
- C'est un peu la même idée que le micro canon. On prend une antenne normale à laquelle on ajoute des éléments qui ne sont pas reliés à elle électriquement. 
##### Antenne directive log periodic
- Appelée aussi antenne "drapeau", "oreilles de Mickey" ou "pelle à tarte"…
- Antenne directive très utilisé comme antenne déportée des appareils (récepteur ou émetteurs)
- Bande passante largeur 
- Remplacé souvent les antennes jouet présentent de base sur les boîtiers de réception/émission 
- Le principe est un peu similaire à la [[Liaisons HF#Yagi|Yagi]]
- Quand on les utilise avec un système de réception diversity, bien penser à les espacer pour pouvoir bien cibler deux directivités différentes et pour ne pas qu'il y ait d'interférences électromagnétiques. (Espacement d'environ 2m)
- Elles se fixent sur des pieds de micro. 

##### Antenne Hélicoïdale
- Antenne très directive, bande passante large et à gain Important 
- Nécessite une bonne orientation
- Souvent utilisée comme émetteur pour les systèmes de retours In-Ear-Monitor (IEM)
##### Variante Hélicoïdale 
- couvre une large bande de fréquence et propose un important 
- Directivité hémisphérique (antenne type hélicoïdale) 
- Utilisée pour les systèmes de retours In-Ear-Monitor(IEM) et l'intercom hf
C'est comme une antenne hélicoïdale mais avec une plaque à l'arrière qui sert de plan de masse (ground plane). 
##### Variante Omnidirectionnelle 
- Utile en réception lorsque le porteur du micro se déplace dans une large zone autour du récepteur (exemple foire commercial)
- Large bande de fréquence.
- On va penser à bien la mettre en hauteur pour être au dessus de tous les dispositifs de la foire ou du lieu ou elle est utilisée. 

>[!note]
>Marques principales d'antennes : 
>- **Shure**
> - **Sennheiser**
> - **RF VENUE** (propose un genre de directivité spécifique (antenne drapeau + antenne fouet))

>[!note]
> - Il existe des antennes actives (avec boîtiers intégré qui permettent un gain électrique jusqu'à +12dB) ou des boîtiers externes (appelés "booster d'antenne")
> - Un passage dans la connection de type BNC, fais baisser le signal de 6dB
> - Permet d'avoir Un meilleur rapport signal bruit (on veut passer au dessus du bruit de fond électronique magnétique) → Si on sort de la zone le démodulateur va générer un bruit blanc. 



### Émetteur (Tx)
- Réalise la modulation (de type FM) de la fréquence porteuse choisie par le signal audio entrant (micro ou) puis émet le signal RF via l'antenne. 
- Connecteur entrée audio : mini-jack, lemo, TA3, TA4… (En fonction des marques et des modèles)
- **Important** : L'utilisateur devra (en plus de choisir une fréquence porteuse entre 470 et 694MHz) régler le gain du signal audio (AF) sur l'émetteur le plus précisément possible afin d'obtenir une qualité optimale (réglage parfois nommé "sensibilité")
>[!note] 
>C'est donc sur le micro (ou parfois le boîtier de récepetion) que l'on règle le gain ! Donc si c'est mal effectué, il faudra agir sur le micro ce qui peut causer des problèmes.
#### Puissance
- Appelé P.A.R. = Puissance Apparente Rayonnée (par l'antenne)
- Exprimée en dBi ou en Watt
- Liaison HF : 30mW (environ 15dBm) **Attention : max autorisé 50mW 
- Émetteur TV : 250kW
#### Traitements audio 
Il sont réalisés dans l'émetteur avant la modulation de la porteuse et l'émission par l'antenne, ils permettent d'optimiser la qualité audio de la liaison HF.
	1. Réduire le bruit de fond lié à la transmission par une pré-accentuation des aigus (qui seront dé-accentués dans le récepteur ainsi que le bruit de fond apparu pendant la transmission).  
	2. **Gérer la dynamique** en utilisant un compresseur à ratio 2:1 pour la réduire de 100 à 50 dB environ (on utilisera un expandeur avec ratio 1:2 dans le récepteur pour rétablir les 100dB de départ). Ce double traitement s'appelle un "**compandeur**" (réalisé en Multibandes dans certains modèles haut de gamme). Parfois le ratio est variable (n:1) en fonction du signal audio = meilleur qualité audio. 
	3. **Empêcher de dépasser le swing autorisé** à 56kHz de variation de la porteuse grâce à un *limiteur*. C'est souvent lui qui impact le plus le son sur les HF analogique. C'est également pour ça qu'il faut vraiment bien régler le gain du micro. 

Les variations de prix de liaisons HF portent souvent sur la qualité des traitements audio. 
#### Exemple d'émetteur de poches
[[Sennheiser G4]] - [[Shure ADX1]] (numérique) - [[Audio limited A10-TX]] (numérique)

>[!note]
>Il existe des modèles d'émetteurs numériques (voir plus paragraphe IV) qui sont équipés d'un enregistreur audio (format carte micro-sd), permettant ainsi d'assurer la prise de son même si la liaison hf avec le récepteur est interrompue ou défaillante. (ex : Zaxcom TRXLA3)

### Récepteur (Rx)
Il assure la réception de la porteuse par l'antenne puis réalise la démodulation de celle-ci afin de restituer le signal audio via une sortie niveau ligne ou micro (

>[!note]
>Attention : Niveau OUT MIC à privilégier afin de ne pas utiliser le préamplificateur du récepteur mais celui de la minette ou de la console.

Certains récepteurs possèdent une fonction "**SCAN**" : Recherche automatique d'une fréquence porteuse libre. On trouve parfois une fonction "**SYNC**" : capteur infra-rouge qui permet d'attribuer la fréquence choisie sur le récepteur directement au micro (que l'on approche du capteur), très pratique pour les plateaux avec beaucoup de HF. 
#### Traitements audio 

![[Liaisons HF 2023-12-06 15.50.59.excalidraw|700]]

#### Squelch 
- Lorsque l'émetteur s'éloigne du récepteur, le niveau de la porteuse diminue jusqu'à se rapprocher du bruit de fond électromagnétique environnant. A ce moment là le circuit de démodulation ne peut plus isoler correctement la porteuse et produit un bruit blanc audio à fort niveau. C'est la limite de la portée de la liaison HF. 
- Le Squelch est une fonction qui agit comme un noise-gâté au niveau de la porteuse (RF) dont l'utilisateur **doit régler correctement le seuil** empêchant ainsi l'apparition brutale du bruit blanc lorsque l'émetteur "décroche"

- Si le seuil est réglé trop haut, on sécurise mais on perd en portée 
- Si le seuil est trop bas, on gagne en porté mais on risque le bruit blanc au décrochage. 
- **Le réglage du squelch s'éffectue sur le récepteur avec l'émetteur éteint**

Le squelch doit être dans l'idéal juste au dessus du bruit de fond. Sinon la coupure ne s'effectuera pas si le seuil est trop bas, ou le mute se fera trop top si le signal de la porteuse perd un peu de niveau si il est trop haut. 
*C'est un gate.* 
Pour régler le squelch il faut éteindre le micro car il ne reste que le bruit de fond : on part avec le seuil le plus haut possible, puis en baissant petit à petit quand on s'approche du bruit de fond le gate va s'ouvrir, il suffit de monter légèrement alors pour être juste au dessus du bruit de fond. Donc ça **se règle**, et surtout avec le **micro éteind**. 
Sur les récepteurs basique : souvent trois réglages du seuil : *High, mid et low*
#### Diversity 
- système à double antenne (A et B) et double circuit de démodulation auquel s'ajoute un comparateur de la meilleure réception entre RF-A et RF-B puis commande le choix en sortie entre l'audio A ou B. Ce système améliore la porté et la stabilité de la liaison hf. 
>[!note]
>Certains systèmes sont vendus comme "diversity" car ils ont deux antennes mais un seul circuit de démodulation, ce qui n'est pas du vrai diversity ! Pour se démarquer les systèmes pro qui l'utilisent réellement affichent le terme "True Diversity". 

Les antennes doivent être orientées à 90° l'une de l'autre. 
Le switch entre les deux canaux est de types crossfade → il est inaudible. 
### Accessoires
#### Câble 
- Coaxial 50$\Omega$ (attention, on ne peut pas utiliser les câble vidéo 75$\Omega$)
- Connecteur BNC
- Le signal RF peut subir une atténuation assez importante en fonction de la longueur du câble (jusqu'à plusieurs dizaines de dB). On ajoute parfois un booster d'antenne (appareil qui ajoute du gain). 
- Il existe plusieurs catégories de câbles avec des performances différentes (A,B,C)
- Câble faible atténuation : *Rigide* et cher (= installation fixe dans bâtiments)
- Un raccord BNC entre 2 câbles provoque une atténuation de 6dB environ. (À éviter)
#### Splitteur et Combinateur (ou coupleur)
- **Splitteur (ou répartiteur)** : Lorsqu'on utilise un nombre important de récepteurs on peut utiliser uniquement 2 antennes raccordées à un répartiteur qui possède plusieurs sorties qui seront connectées aux entrées RF-in des différents récepteurs. Il existe des répartiteurs passifs ou actifs. (Ils ont un booster intégré)
- **Combinateur** : Lorsque l'on utilise plusieurs appareils émetteurs (pour des IEM par exemple) on peut utiliser uniquement 1 seule antenne qui reçoit les signaux RF à émettre depuis le combiner auquel on a connecté toutes les sorties antennes RF-out des différents émetteurs. 
- C'est appareils permettent d'éviter la multiplication des antennes situées les unes sur au-dessus des autres dans les racks évitant ainsi les problèmes de rayonnement qui parasitent les antennes entre-elles. 
##### Exemples 
- Splitter 2 antennes Sennheiser 
Ajouter schéma 
- Combinateur 1 antenne Sennheiser
Ajouter schéma 

>[!note]
>On peut distribuer le signal d'une antenne directement grâce à une sortie RF (ou Cascade) 
>Il y a en effet des émetteur ou récepteurs avec les deux RF-in et RF-out ce qui permet un branchement en cascade. (Il y a autre une petite compensation, mais il y a une limite aux nombres d'appareils en cascade)

### In-ear monitor (IEM)
C'est un système de retour sans fil avec oreillette
- Utilisé en concert et à la tv
- L'ingénieur du son aura la gestion de l'émetteur et la personne utilisant l'oreillette sera équipée du récepteur de poche. Attention à la **gestion des niveaux sonores par l'ingé son !!!**
- Possibilité de transmettre un signal stéréo multiplexé sur la même porteuse (sur certains modèles). 
- Mode Mix permettant au musicien de régler sur le récepteur le mélange mono entre CH1 et CH2 (ex : CH1 = mix et CH2 = instrument seul du musicien concerné)
#### Exemple 
Système shure PSM900

#### Notes 
Certains groupes mettent les amplis en backstages et utilisent de "faux ampli sur scène" pour isoler le son de ceux-si. 

Penser à mettre la salle dans les ears. 

Pour les bassistes parfois on met des shakers sous la scène : C'est des haut parleur que l'on visse sous la scène, pour diffuser des basses de façon localisées sur le plateau. 

>[!note]
>Pensez à mettre un limiteur sur les aux qui partent dans un ear monitor. Permet d'éviter d'exploser les oreilles des musiciens
>Quand on fait des retour demander : **Qu'est ce qu'il te manque** plutôt que tu veux quoi → Le force à écouter le mix et pas dire bah un peu de tout. 

### Intermodulation
- Perturbations dues à la présence de plusieurs fréquences porteuse en simultané.
- Augmente le bruit de fond électromagnétique. 
- Précautions : Éloigner les antennes des émetteurs, coupler les antennes si plusieurs récepteurs ou émetteurs, ne pas émettre à niveau de puissance trop élevé. 
- *Idéalement* : choisir uniquement les fréquences proposées dans la même banque (ou groupe) proposée par le constructeur, ou concevoir un plan de fréquences en utilisant un logiciel de calcul de fréquences d'intermodulation.  (Banque ou groupe c'est en fonction de la marque, qui nomme différemment la même chose)
- Ex : Si F1 = 600MHz et F2 = 585MHz alors problème à 2F1 = F2 = 615MHz (ordre 3) et à 2F2-F1 = 570MHz (ordre 3). Donc attention au choix de fréquence si on utilise un 3ème choisie.

>[!note]
>Il faut prendre des fréquences du même groupe ou banque ! Il ne faut surtout pas prendre des banques différentes. 


## Exploitation
### Organismes et réglementation 
Indispensables pour éviter l'encombrement
- UIT : Union Internationale des Communications (attribution, planification des bandes)
- CMR : Conférence Mondiale des Radiocommunications (coordonne les bandes HF et VHF en 3 zones : 1 : Europe | 2 : Amérique | 3 : Asie)
- CEPT : Commission Européenne des Postes et Télécommunications 
- *France* : 
	- ANFR : Agence Nationale des Fréquences (répartit les fréquences sur le territoire) www.anfr.fr
	- ARCEP : Autorité de Régulation des Communications Électroniques et des POstes (les liaisons hf pro sont soumise à cet organisme : www.arcep.fr). Les bandes autorisées sont ensuite gérées par le CSA (Conseil Supérieur de l'Audiovisuel) devenu aujourd'hui l'ARCOM 
>[!note]
>Les utilisateurs sont classés en 3 catégories avec des niveaux de priorité : 
>A : Société nationales de programmes TV et radio
>B : Autres éditeurs de to ou radio conventionnés par l'ARCOM 
>C : Sites fixes, sociétés de location et prestation

### Occupation des fréquences 
- Afin de choisir une ou plusieurs fréquences libre pour les liaison hf dans un endroit donné, il existe des logiciels d'aide et de scanneur de l'environnement électromagnétique. Certains logiciels sont développés par les fabricants de liaisons hf comme *Shure : Workbench ou Sennheiser : WSM*. Ces logiciels permettent également de contrôler via liaison ethernet les différents appareils d'un systèmes simple ou complexe. Des applications mobiles sont également développés par certaines marques de matèriel HF : Channels de Shure ou encore WSM et Smart Assist de Sennheiser. 
- Il existe aussi des sites internets qui permettent de connaître l'occupation des fréquences par la TNT (Télévision Numérique Terrestre) ou la téléphonie mobile : www.scanzone.fr
- *Fenêtre Scanzone* 
<iframe src="https://www.scanzone.fr/fr/transmitters/display/place/19180" width="'600"></iframe>



