---
Matière:
  - Technologie des Equipements
  - Pratique
Semestre: B2-1
Date: 2023-11-08
Prof: "[[Ruddy Palmier]]"
Type: notes de cours
tags:
  - cours
  - Technologie-des-équipements
---
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