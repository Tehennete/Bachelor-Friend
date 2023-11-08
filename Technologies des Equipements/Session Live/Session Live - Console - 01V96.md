---
Matière: 
- Technologie des Equipements
- Pratique
Semestre: B2-1
Date: 2023-11-08
Prof: Ruddy Palmier
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
# Session Live - Console - 01V96
Date: [[2023-11-08]] ## Hardware Console 
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
#### Pairer les Stéréo

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

#### 2-track
Patch → Onglet 2-tracks

2-track in ou le 2-track Output 


### Pendant le REC 
Il faudra un bon niveau pour le HDP2. 