---
aliases: 
Matière: 
Semestre: 
Date: 2024-10-17
Prof: 
Type: notes de cours
tags:
  - cours
---
# Ableton live 1
Date: [[2024-10-17]] 

Live a été crée par des musiciens pour des musiciens	 
Il a été fait en 2001 par des allemands, issus de la scene electro 

3 tarifs : 
Intro | Standard | Suite 
### Live 12 
Compatibilité ascendante = oui | Descendante = non

2 fenêtres :
- Arrange → Montage linéaire 
- Mix \ Session → Non linéaire / séquentiel 
**TAB** pour changer de fenêtre 

Volet de gauche = bibliothèque 
**CMD + ALT + B** (Comme biblio)

Éditeur audio / MIDI 
**CMD + ALT + L**

Volet droit pas important pour la session en cours sauf pour des fichiers manquants

Overview : **CMD + ALT + O** qui fonctionne comme l'univers de [[Protools]]
Il suffit de cliquer et d'aller en haut ou en bas sur l'univers pour zoomer.

Mix que l'on peut obtenir meme dans la fenêtre d'arrangement (Version 12 seulement)
**CMD + ALT + M** (Comme mixeur)

### Icône du haut
En haut à droite

Link - pour faire un lien avec d'autres application 
Tap - Tempo - click pour faire un tempo different 
2 points = metronome - on peut choisir la métrique et le son
Les bars avant c'est pour se synchroniser avec des platines 
Ensuite dans la version 12 on peut choisir la gamme 
Les gammes ne feront apparaître que les notes de la gamme choisie. 
Time line 
Play stop record 
Ensuite gestion d'automation 
Loop **CMD + L** → On fait une selection et on fait le raccourcis pour mettre la selection en boucle 

A droite 
Crayon qui permet de dessiner notes midi / automation → Touche **B**
Clavier permet de transformer le clavier du PC en clavier midi. 
On peut changer d'octave avec **w et x** et changer la vélocité avec **c et v**


>[!note]
>Perle de Stala :On va écouter le poisson le poisson

Le Bouton "Key" **CMD + K** → Permet d'attribuer une touche du clavier pour faire un raccourcis sur un paramètre qui s'allume en orange
Le Bouton "Midi" **CMD + M** → Permet d'attribuer une touche midi sur un paramètre qui s'allume en bleu 

>[!note] 
>Par exemple mettre la molette sur le fader pour faire de l'automation 

Retour à valeur initiale : supprimer ou double clique 

Les raccourcis sont listés dans la bibliothèque. 

Si on veut garder les valeur → Fichier > Sauvegarder le Set Live Par default (Modèle qu'on aura quand on lance Live)
Bien de se faire un modèle par default 
### Fenêtre d'arrange 
Les numéros des permettent de mute / unmute les pistes 
Pour grouper des pistes : **CMD + G**

#### Routing 
Audio from → le son vient 
Audio To → Ou le son va 
On peut envoyer des pistes dans une autre piste

Créer une piste : 
**CMD + T** = Piste Audio 
**CMD + SHIFT + T** = Piste MIDI 
**CMD + ALT + T** = Piste de retour 

Renommer : **CMD + R**

Sur les pistes retour on peut mettre chaque retour en pre/post sur TOUTES les pistes d'un coup. 

#### Zoom Vertical 
Selection des pistes → **ALT + +/-** ou **ALT Molette**
Horizontal meme chose avec **CMD**

Remettre à 0 → **H / W** ou en bas à droite de la fenêtre 
Permet d'afficher l'entièreté de la session et remettre l'affichage à 0 

Zoomer les formes d'ondes qui se trouve en bas à coté de "H et W"  (Que sur le 12)

#### Grille 
Adaptative en fonction du zoom ou grille fixe 
Changer de taille de grille **CMD + 1 / 2**

#### Faders 
En appuyant sur **SHIFT** on passe en variations par décimales 

#### Sélections 
Dans la forme d'onde 
Si on fait une sélection et qu'on prend l'étiquette il va automatiquement découper le clip 
→ Manipuler / Trimer = c'est l'étiquette
#### Automation 
Mode auto : A 

#### Time Stretch 
Comme le trim mais avec **SHIFT** en plus 
(Il faut que le warp soit activé)

#### Mode similaire au mode shuffle de ptx 
Si on colle une durée → **CMD + SHIFT + V** va coller le vide sur toutes les pistes (Insére le collage)
**CMD + SHIFT + X** Coupe comme le mode shuffle 
**CMD + SHIFT + suppr** supprime comme mode shuffle 

### Bibliothèque 


### Live Set 
Toujours créer un live set et bien définir ou il se trouvera 
Ableton Project Info → C'est les options de la session (à ne pas toucher)
Fichier .als → Fichier live (Double click dessus lance la session )
Backup : sauvegarde 
Pour mettre les samples fonction indispensable : qui permet de rassembler tout l'audio dans la session : 
**Fichier → Réunir et sauvegarder** (Pas automatique) → On peut le faire avec des macros 
Sample (Imported/Processed/Recorded) : La ou se trouve les fichiers audio 
Sauver : **CMD + S** 
### Éditeur midi 
Alt avec crayon verrouille 
Casque permet d'écouter la note que l'on joue

### Export 

**CMD + SHIFT + R** (Comme render)
Piste convertie permet de faire un rendu du master (Main) ou de toutes les pistes (Pour faire des stems par exemples)

### Print 

On cree une piste → Audio from → Resampling (Il va enregistrer tout ce qui passe dedans.)