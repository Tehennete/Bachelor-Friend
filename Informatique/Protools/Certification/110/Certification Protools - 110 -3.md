---
aliases: 
Matière:
  - Protools
Semestre:
  - B2-2
Date: 2024-04-17
Prof: "[[Alexandre Badagee]]"
Type: notes de cours
tags:
  - cours
  - protools
---
# Certification Protools - 110 -3
Date: [[2024-04-17]] 

# Chapitre 9 : Post-prod
Son à l'image 
### Timecode et FPS
Session setup CMD + 2 
Time code et frame rate 
En France on est dans la zone PAL = 25 fps 
Zone NTSC = 23,976 fps soit du 29,97 fps
Cinéma = 24 fps peut importe la zone 
Pour les format HD 

Dans session setup on peut régler le time code rate. 
On met un double time code pour avoir une 
En main unit on peut pas mettre le Time code 2 

Si on met 

Protools intro et protools artiste on ne peut pas gérer la video 
Protools studio on peut avoir qu'une seule piste video, on ne peut pas éditer le fichier video 
Protools ultimate : on peut avoir 64 pistes video (une seule lut à la fois) on peut éditer le fichier video.

Menu > Setup > playback engine > Video engine doit être activé 

pour importer une video
SHIT + ALT + CMD + I  
Ou menu > File > Import > video 

Format possible d'importer dans protools 
- MOV 
- H264
- H265
- MP4 
- MXL video

CMD + 9numpad permet d'afficher la fenetre video. 
J'ai manqué un truc

2 types de vue 
- bloc on voit juste la piste pas de miniatures 
- Frames → montre des miniatures
On retrouve le framerate dans les info de pistes. Si le frame rate est en rouge alors c'est que les framerates ne sont pas synchro 
Si on importe une video protools va automatiquement synchro les deux fps

On peut ajuster les performances 

Clic droit sur la fenêtre video, cela donne le choix de la taille et on a aussi le choix de la qualité. 

Si on doit placer la video à un time code précis : 
On prend le mode spot, en cliquant sur la video on peut déplacer la video la où on veut ou au time code qui est indiqué/affiché sur la video

### Déplacement de fichiers 
Pour déplacer un clip : 
**CTRL + Clic** sur un clip : synchronise le debut du clip sur le curseur ou le debut du clip déjà sélectionné
**CTRL + CMD + Clic** : meme chose mais avec la fin du clip 

Quand c'est un point a l'intérieur 
Créer un point de synchro (marker avec ancre verte) CMD + ","
Menu clip identify sync point

Même chose que les deux premiers mais en déplaçant le clip par rapport au point de synchro : 
**SHIFT + CTRL + clic**

### Clip effect 
**ALT + 6numpad**
Onglet en bas de l'édit window. 
Clip effect comme le clip gain. Il est indépendant pour chaque clip de ma session. 
Cela évite les automations. 
Il est basé sur les modules du channel strip 

On voit qu'un clip est modifié par le clip effect en haut à droite de clip. (EQ, DYN, $\Phi$ )

Clic droit sur le clip permet de retrouver des Options du clip effect :
- bypass
- Copy
- Clear 
- Render (Encapsulage)
On retrouve la meme chose dans le menu clip mais sans la capacité de clear. 

On peut enregistrer des configurations de clip effect 
CMD + Clic sur un des numéros. 
Save settings pour plus de templates sauver. 

Menu setup preference > a la place de zoom preset on met clip effects 
Dans d'ancienne versions le clip effect au meme endroit du universe. 

On peut maintenant sortir le clip effect. 

# Chapitre 10 : Mixage

Si je veux rajouter des sorties supplémentaires : J'appuie sur **CTRL** avant de cliquer sur les sorties, cela les ajoutera à la sortie déjà définie. 
On le sait car devant la sortie il y a un plus → Affectée à au moins deux sorties 

Si on a un Astérix : Notre piste sort au minimum  par deux bus différents mais il y a au moins un des deux qui est inactif. 
C'est un miroir de piste.

On peut faire des miroirs de bus aussi 
Setup > I/O > Output 
on peut faire CTRL et cliquer sur les sorties que l'on veut ajouter au bus. 

On a donc deux options : Miroir de bus ou miroir de sortie 
Ne marche pas avec les entrées 

[[610A]]

>[!note]
>Ne pas mettre de plug sur le master fader car les inserts sont post fader donc si on baisse on change le comportement des plugins ! 
>Le master fader gère le niveau de sortie du bus qu'il control. 


### Envoies 
L'envoie de base est de base post-fader → Flèche grise, la flèche devient bleue en pre-fader.

Setup > pref > mixing > sends default to : on choisit la valeur 
Attention des règles de sécurité : en Rec on ne coche jamais l'option. Car les circuit de casque peuvent éclater les oreilles des musiciens. 
**CMD + Clic** sur la flèche (sur le non ça mute l'envoie) → Ouvre l'expended view 
Pour ouvrir tous les expended view **ALT + CMD + CLIC** 

Ou view > expended sends 
On peut avoir accès au niveau, au mute, au pre/post et au pan. 

Quand on clique sur le nom du bus on a le nom de la piste sur laquelle le sends se trouve, on peut alors changer le sends dont on regarde le niveau, on peut choisir aussi le bus. 
Il y a ensuite les options : 
- Post/pre
- Les pans sont indépendant sauf quand on clic su FMP (Follow main pan) qui fera correspondre le pan du sends au pan de la piste 
- Safe : Va interdire toute automation dynamique, il verrouille l'automation dynamique mais il laisse la capacité a faire des automation statique (pencil ou grabber)

Sur les envoies stereo sur une pistes stereo : 
- le premier va linker le pan de droite et gauche dans le meme sens 
- Permet d'ajouter le sens inverse au link precedent (les deux boutons)

### Automation 
Les modes : 
- read : lit les automations 
- Désactivé/OFF : ne les lit pas 
- Write : écrit du debut a la fin 
Setup > pref > mixing after write pt peut changer le mode automatiquement. 
Déconseillé de rester en mode write car lors d'une lecture après on va écraser ce qu'on vient de faire. 
- Latch : on entre en écriture que quand on touche le paramètre 
- Touch : on entre en automation que quand on touche le paramètre  et il revient avec une latence vers le volume initiale. Le temps de retour est réglable 
Auto-match time se règle dans preferences > mixing > auto match time
Par défaut 250ms
- touch and latch : le volume est en touch tous les autres sont en latch

#### Fenêtre d'automation 
CMD + 4numpad 
Ou menu > win > automation 

Suspend va empêcher toute lecture et écriture d'automation. Cela revient a mettre toutes les pistes en OFF 

Crite enable va autoriser ou suspendre l'écriture en fonction des types de paramètres. 

#### Copier coller des automations 
On peut copier des automations  **CMD + C/V**
On peut demander de copier de façon spécifique les diverses automation d'une piste 
Menu > edit > copy special 

Le past special exist aussi pour pouvoir 
**ALT + CMD + V**  cela va remplir la selection avec l'automation : Repeat to fill selection 

** ** permet de coller une automation sur n'importe qu'elle type d'automation sur laquelle on est. 
To current automation type 

Merge midi ne s'applique qu'aux contenus midi. 

Avec la fonction cut, PT crée un breakpoint au bord de chaque extrememités de la selection, 

Clear va effacer les points, donc pas de breakpoint donc les breakpoint seront ceux les plus proches de la selection qui feront la courbe. 

Une automation peut être nudges avec le **"+" et "-"** du numpad  ou les touche **, et .** (en qwerty) Ou **; et :** en azerty 

Si on veut suspendre une playliste d'automation : **CMD + Clic** = suspendre la playliste d'automation. 

### Groupes 
**CTRL + CMD + G** permet de modifier le groupe 

Si on clic sur la couleur du group Pt va sélectionner les pistes appartenant au groupe 
On a pas besoin pour ça que le groupe soit actif. 

- Point devant un groupe sa veut dire que toutes les pistes du groupe sont selectionnées
- Cercle devant un groupe : au moins une piste du groupe n'est pas sélectionnée 
- Cercle avec un point a l'intérieur : Toutes les pistes du groupe + au moins une piste hors du groupe 
Si on appuie sur les lettre correspondant au groupe dans la fenetre de mix cela permet d'activer le groupe  la premiere banque de groupe 
SHIFT + ! (1 de l'alpha num) (Pas equivalent azerty) active désactive le groupe all 

Maintenir CTRL permet de bouger un fader sans que les autres faders du groupe bougent. 

### Routing folder track 

**SHIFT + ALT + CMD + N** envoie la piste vers un nouveau folder track 
ou clic droit move to : 
- soit new 
- Soit folder existant 

Sortir une piste d'un folder clic droit sur la piste > move to > Top level 

Ou alors drag n drop pour entrer ou sortir. 

Sur des anciennes session, les sous groupes peuvent être des auxiliaires. 
On peut les convertir en routing folder track 
Clic droit sur le nom de la piste 
Menu track convert aux to routing folder track 

Pas possible de faire l'inverse. 

Quand on mute ou solo on met en solo toutes les pistes à l'intérieur sauf pour les pistes déjà mutées ou inactive 

### Export 
Quand on export d'un higher bitrate a un lower bitrate 

Quand on bounce on doit mettre un plugin de dithering en dernier dans la chaîne de traitement du bus master mais pas si tu print sur une piste audio. 

SI on utilise l'export clip as file. PT va placer de lui meme un dither sur l'export. 

### Nettoyage de session pour archivage 

Menu clip list > select : 
- unused **SHIFT + CMD + U** selection les fichiers dans la clips liste qui ne sont pas 
- Unused except whole file : sélectionne que les sub clip 
- Offline : tous les fichiers pas retrouvé par pt dans la timeline ou la clip list

**SHIFT CMD + B** ou clear dans le menu de la clip list 

Trois options : subset clip et whole files 
- remove : enlève juste de la session 
- Move to track : enlève de la session et place dans la corbeille 
- Delete : enlève de la session sans passer par la corbeille 
Que des subset clip : 1 seule option de clear 

Pour tout valider en une fois ALT + Clic

On peut aussi compacter la session 
**SHIFT + CMD + A** 

On peut ensuite faire la fonction compacter 
PT Va analyser les fichiers de la clip list, va mettre un pad d'une durée définissable et va enlever les morceaux non utilisés dans la time line. 

On le fait après avoir nettoyé 

## ILOCK 
Protection anti copie 
Posséder un compte Avid 
Il faut créer un compte ILOCK  et declarer un identifiant
La license avid va être envoyé sur le compte ILOCK. On le voit apparaître sur le compte ILOCK manager
Il faut ensuite installer en local ILOCK manager 

