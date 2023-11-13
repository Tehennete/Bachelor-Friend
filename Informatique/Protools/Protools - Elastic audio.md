---
Matière: Technique Protools
Semestre: B2-1
Date: 2023-10-12
Prof: Stalla
Type: notes de cours
---
# Elastic audio
Date: [[2023-10-12 1]] | Tags : #cours #protools

C'est découpé en 2 catégories : 
- Elastic time (time stretch) → c'est la durée
- Elastic Pitch (hauteur/correction) → C'est la variation de hauteur de la Note
## Élastic Time
### 1 Choix de l'algorithme
C'est au niveau de l'en-tête de piste avec un contenu audio. Au niveau du marqueur de warp. 
Cela donne un menu avec : 
**Temps réel :**
	- polyphonic → généraliste
	- Rhythmic → percus
	- Monophonic → plus précis mais ne permet pas de changer de pitch
	- Varispeed → Hauteur en fonction du BPM (effet platine)
**Rendu :**
	- X-form (rendu uniquement) → plus performant mais pas en temps réel, c'est un rendu en différé (à utiliser quand on est pas satisfait des 4 premiers) 
En bas du menu on peut choisir le mode de traitement : en temps réel  ou en rendu (c'est pas disruptif comme audio suite)

>[!NOTE]
>Le TCE fait des rendus destructifs s'il n'y a pas d'algorithme d'élastic audio, donc bien penser à définir l'algorithme avant d'utiliser le TCE.

Quand on dépasse les limites de déformation, il l'affiche en rouge sur la piste. 
### Choix de la Timebase
- [1] En sample

→ échantillon : Absolue
Utilisée principalement pour les sons qui ne dépende pas du BPM
- [2] En Ticks 

→ Son musical qui varie en fonction du BPM

## Elastic Pitch 
**Alt-5** : ouvre propriétés elastic (clip>propriété elastic)
Les propriété de pitch sont en temps réel (meilleur que sur les plugins audio suite de pitch)

Formant, c'est la taille du larynx, donc ça permet de changer la voix plus naturellement.

> [!note]
>  Déformation dans l'affichage des pistes c'est le Warp

## Identify Beat (cmd - i)
**CMD + i** → ouvre l'identifier de tempo.
On rentre le début, de la mesure on fias 3 Fois la touche tab puis on choisit la mesure de fin

## Pour quitter elastic audio 
C'est dans le menu de selection du mode algorithmique → Il faut sélectionner :
Aucun traitement - désactiver → deux choix 
Soit on valide et il rend les fichiers (pour alléger le processeur quand on a fini)
Soit on restaure et on retrouve les valeurs initiales des fichiesr

## Sélection à la volée
Flèche du bas → point d'entrée
Flèche du haut → point de sortie
On peut ajouter la selection avec les flèches bleues sur l'univers (la ligne au dessus des pistes)


[[Raccourcis Protools]]
