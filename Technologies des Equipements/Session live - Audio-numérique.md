---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-12
Prof: Ruddy Palmier
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Audio-numérique
Date: [[2023-10-23]] 

## ADAT
Entrées Et sorties → Pas le même câble
8 canaux 24bits/48Khz (4 canaux S-MUX 96Khz)
En Toslink 
Wordclock → Sync → Master/slave → BNC extérieur / Toslink (compris par l'Adam) → ON privilégie la BNC car selon les flux généré, On va délesté l'ADAT et donc il n'y aura que les informations importants dedans. (En général, on utilise les deux par sécurité)

Worldclock → Horloge Ext → Apogee / Crystal (PMZ)
L'horloge donne le taux de précision des machines. 

Choix a faire sur les carte sons → Regarder la meilleur horloge du marché et voir lesquelles en sont équipées. 

Dans l'exercice on va utiliser l'ADAT sur la console. Sur la console on va utiliser beaucoup de pistes. 
Sur tout matériel ADAT dispose d'une horloge interne. SI j'ai une carte UAD et une carte RME je peux dire que l'ADAT gèrera la clock pour ma carte principale qui le distribuera à mon UAD (horloge de moindre qualité). 

>[!NOTE]
>Seul cadre ou on risque d'utiliser le time code c'est quand on fait de la post-production cinéma ou télé. Sinon on le branche simplement sur notre machine (TC issue des caméras ou des appareils d'images)

## Régie REC 
Protools 
- 16 canaux inputs 
- Une sortie playback → pour réécouter les prises → sur les enceintes
- Une sortie click

**L'objectif de la régie REC**
Le choix des préamplificateurs et un bon niveau de REC → (Gain)
Une fois que le gain est fait on ne le touche plus. 
Le but c'est d'avoir des niveaux convenables. 
### Pré-amplification
Différentes fonctions 
- High-Pass
- Low-Pass
- +48V
- AIR (spécificité AIR) → Émule un high-shelf (aux alentours de 10k)
- PAD (avant -15dB sur du vintage) → Atténuateur entre -15 et -20dB 
- $\emptyset$ → à utiliser si le câble est inversé avec un micro (on a des pertes de graves si ça arrive) → ou quand on a plusieurs micro (snare)

Woodstock → Deux micros chants pour en mettre un en phase et l'autre hors-phase pour ne pas rec les bruits du publics.
Bruit dans un lieux → on l'enregistre et on le mais dans le mix en inversion de phase. 

Si on veut faire du Re amping quelle préamplificateurs utiliser ? 
### Création projet protools (session)
Mettre la tonalité du morceau, l'indication de refrain, de couplet, le tempo, etc…
→ Se créer un template
Pour ce projet : 
7-8 → Sorties analogiques vers les enceintes et 6 uniquement le clic. Pas d'autre sorties utilisés

Souvent les 8 premières sorties sont analogiques → 9-10 = SPDIF
### Hardware pour le REC
Penser à réinitialiser les appareils → tout remettre à 0 
Peut importe le hardware → Le remettre à zéro si ce n'est pas toi qui ait utilisé avant. 

>[!NOTE]
>La synchro ADAT ne se fait jamais automatiquement → Il faut toujours choisir qui est maitre/ ou si c'est en autonome

#### Focusrite 
Sur le logiciel de routine focusrite :
Faire attention que la sortie Casque ne soit pas "DIMé"
Le loop back c'est un système de Réamping interne à la carte son. 
####  Amp behringer ultragain digital
Va être utilisé pour la partie Live et pas REC.
Led en Vert = signal à -20dB et Rouge = Clip
#### Midas XL48
Les vus-mètres or préamplificateurs indique si la liaison se passe bien.
Différentes positions changeables avec un switch.

Les différentes positions indiquent : 
- Les fréquences d'échantillonnage
	44.1
	48
	88.2
	96
- La synchro (vert c'est bon, rouge c'est faux)
	Sync in
	Sync out 

Lien entre focusrite et midas XL48 → ADAT toslink + BNC pour le clock

Selon la sortie d'enceinte → Brancher les enceintes en numérique (édirols). {En s/PDIF}
Le jour J, c'est à notre charge. 

Proposition de patch → Fin de semaine impératif → Patch protools (quels préamps)

Donc il faut deux patch (scène/protools)
### Hardware Console 
On va ajouter une extension Behringer sur la console Yamaha → Pour les connecter : toslink + BNC (ADAT + Wordclock)

À faire pour la synchro → Vérifier que c'est bien la console qui donne le WC
Si les deux machines sont en mode master il y aura un message d'erreur sur la console. 
Pour le Wordclock c'est avec le bouton : **Display accès →** **Utility** 
#### In-Patch

Pour gérer le routing : **Display access → Patch**
AD = pré-amp de la console. 
Pour configurer l'Adat il suffit de tourner la molette pour sélectionner l'entrée **ADAT**
Sur l'AD 9 on peut choisir de mettre de l'ADAT 1 par exemple. 

Le Behringer est très versatile (comme la focusrite), il est moins marqué que les préamplificateurs de la console 

**Talkback sur l'ADAT 8**

#### Output patch 
*Dans un onglet*
Même chose, tout est configurable. Les sorties ADAT sont mentionnées. Les sorties 1 à 8 sont assignables à la sortie de notre choix. 8 aux, ou la sortie est selectionnables.
Les omni out peuvent être 

Objectifs : 
Faire un patch 
Synchroniser les machines 
Maîtriser le routing c'est la base → Maîtriser le signal et équaliser pour que ce soit clean dans les oreilles. Avec en plus caler une plate dans la voix.
#### Pairer les Stéréoptique 

Display Access → Pair 
Ensuite on choisit les voies que l'on veut appairer. Elles sont appairés aux faders et EQ. tous le reste (gain, pan) ne seront pas impacter. 

Bien penser à checker et reset manuellement la console. 
#### Les effets
**display Access → Effects**
Bouton pour se balader entre les types d'effets et le routings de ceux-ci. 
LIBRARY pour entrer dedans on sort avec la fenêtre ÉDIT. 
Le patch ce fait en interne → Bouton patch de l'écran. 

Objectif : Plate 
Avec le juggle wheel on peut choisir quel aux aura l'effet. 
Choisir un départ mono. (Car instrument mono) → Aux 7 
Le retour on peut le faire sur le stéréo in. Mais la on va prendre une sortie qui sera en 31-32 → On va les pairer. (Ils marchent pas sur la console).  On choisit les tranches à afficher sur : **Layers** 
Bien penser à mettre le fader ON 

Regarder les trucs disponibles dans la librairie.
##### Layers 
1-16 : Le premier numéro sous le fader 
17-32 : le deuxième sous les faders
Master : c'est celui qui est marqué en dernier sous les faders

#### Le traitement 
C'est dans **Display Accès → View** 
La page de pan s'affiche dès que tu fais un pan. 
parameter → affiche toutes les options de ta console.

2 types d'equalisations : 
- un EQ grossier
- Un EQ plus fin. 
Bouton pour changer la phase. 
La possibilité d'appairer directement depuis la fenêtre. 
De mettre du delay (positionnement des micros)
C'est en haut que l'on c'est sur quelle page on est.
Tous les effets s'affiche sur l'overview. C'est la qu'on voit la compression etc….
On retrouves tous les détails de la tranche. 

Aller sur EQ edit pour plus de précision.

EQ comme sur Protools (niveau de sortie et d'entrée reglable)
#### EQ edit 
**display access → EQ**

Le low cut se fait directement dans l'EQ utiliser la bande low (ou high pour high cut)
On fait soit un Low cut soit un high shelf. 
En fonction de la bande sélectionner. 
Donc on perd une bande. 

#### Comme c'est connecté au HDP2 
Il faut que ça sonne aux oreilles. 
Il faut que l'omelette soit mangeable

→ Faire un gain, equalisé, comp possible, reverb sur la voix du lead. 
 et également,t faire l'envoie sur les aux. 

Soit à la Mano soit en send on-faders
#### Sends on faders 
Dans un des sous menu du view. 
On sélectionne notre aux. 
Les faders deviennent des sends. 
Seule chose à vérifier : Tout en mode all nominal → Tous les faders à 0 
Pouvoir choisir si TOUS Les entrées en envoies soient en pré ou post fader. 
Tous les envoies sur l'aux 1 seront en pré ou post. 

Pré-point permet de mettre tout le monde on ou off → car pour envoyer il faut être en on. 
Le talkback doit être en pré fader. → sert qu'au circuit retour. 

Bien penser à mettre en ON les tranches d'envoi et le fader de l'aux (LAYER→Master)
Et mettre le fader de l'aux à 0 ils sont en bleu
#### Solo 
Pour activer le solo il faut que la tranche soit ON et sur 0 
Solo clear (bouton) enleve tous les retours. 
#### Sortie master 
On va enregistrer la sortie master sur le HDP2
#### HOME 
Bouton important quand on fait les gains. 
Car permet un VU mètre de tous les gains 
Sinon il y a juste la led qui signal le -20dB et le PEAK

Quand on fait le gain, penser que les EQ altèrent le gain → penser à adapter le niveau après les EQ

### Sur Protools
#### Création de session
48k 24bits 

Première chose à vérifier c'est le moteur de lecture. 
Bien le mettre sur la bonne carte son.
##### entrées
Dans les entrée loop c'est propre à focusrite. 
Par déduction on a trouvé que le 9-10 correspondait au SPDIF → le check quand même
##### sorties 
Sur laquelle on va mettre le clic
##### bus 
On ne va pas utiliser les bus. 

##### Le clic 
On ne vas pas lui mettre de sortie de base, on va l'envoyer dans une des sorties de la carte avec un send. 
