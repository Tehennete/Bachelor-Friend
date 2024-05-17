---
aliases: 
Matière:
  - Protools
Semestre:
  - B2-2
Date: 2024-04-16
Prof: "[[Alexandre Badagee]]"
Type: notes de cours
tags:
  - cours
---
# Certification protools - 110 - 2
Date: [[2024-04-16]] 

# Chapitre 5 

Alléger le CPU, elastic audio et clip gain 
## Alléger le CPU 
### Fonction Freeze 

On peut freeze les piste audio - instrument - aux et routing folder tracks 
On ne peut pas freeze les VCA basique folder track et pistes master fader

On peut soit cliquer sur le snow flake, soit menu track>freeze, soit clic droit freeze 
Il est cumulable avec les actions alt et shift alt 

Des qu'au moins une piste de la session est freezer : 
- on ne peut plus changer le tempo 
- On ne peut pas éditer le fichier. 
- On peut utiliser les parametres  qui ne sont pas freezés et donc utiliser des **automations** (De volume par exemple)
- Accès aux sends 
- Accès aux sorties mais **pas aux entrées** 

Quand on freeze on ne crée pas de fichier dans audio files mais dans le **rendered files** 
Normalement se doit être des fichiers temporaires. 
Les fichiers ne sont pas temporaire officiellement ils restent dans le dossier rendered files. 

### Commit 
Pour commit une selection : **SHIFT + ALT + C**  
Ou clic droit sur la piste commit ou menu-track-commit

Cela permet de commit l'intégralité de la piste ou juste une selection 
On peut commit **post fader ou pre fader** On peut aussi prendre le panoramique. 

Une piste mono qui est commit sera transformée en piste stéréo si on coche la case panoramique. Sinon elle restera mono. 

La piste source peut soit rester comme elle est, elle devient inactive, elle devient inactive et cachée ou on la delete. 

Attention cela crée une autre pistes avec des nouveaux fichiers audios qui sont dans le fichier audio files. 

Quand on fait une operation de commit : 
- garde le clip gain on encapsule le clip gain
- Ne garde pas l'elastique audio (encapsulé)

### Track bounce 

≠ de bounce mix (ALT-CMD-B)
**SHIFT + ALT + CMD + B** 
Ou clic droit sur le nom de la piste ou menu track bounce. 

On peut bouncer : 
- Audio 
- Aux 
- Instrument 
- Routing folder track 
- Master fader 
On ne peut pas bouncer : MIDI et Basic folder 

Quand on fait track bounce cela va dans le dossier bounced files 

Les differences avec le bounce mix : 
Dans bounce mix on doit choisir une sortie 
Dans bounce track on choisit les pistes sélectionnée 

Le nom sera le nom du prefix 
Nom = Prefix_nom de la piste_ST/M

Il peut être préfader ou post fader (option cochée)
On peut prendre en compte le pan ou non. 

Il est selection base → Part du debut de la selection  jusqu'à la fin. Sinon début de session jusqu'à la fin de la session. 

Pad to frame boundary → pour un envoie pour de la video. 

On peut importer les bounces dans la session sauf si on change la fréquence d'échantillonnage. 

C'est trois manipes de processes permettent de sauver du cpu. 

Commit et freeze plutôt en phase de mix 
Commit pour exporter pour en phase de mix 

Track bounce export de multi track pour le mixeur. 

## Clip gain 

Tous les raccourcis seront a base de SHIFT CTRL 

LE clip gain sera pré-tout 
Pre-insert, pre-send etc… 
Il s'étend de -144dB à + 36dB 

Il va pouvoir être statique si tout un clip est modifier par la meme valeur 
Il va pouvoir être dynamique si la modification n'est pas identique tout le long du clip. 
Clip gain mixte application d'un clip gain statique sur un clip qui a été modifier avec un clip gain dynamique. 

On peut afficher des info 
Menu>view>clip 
Affiche le clip gain info en bas à gauche du clip 
**SHIFT + CTRL + "="**  (SHIFT + CTRL + "-" AZERTY)

Clip gain line 
Un seul par clip. 
Cela va se croiser entre qwerty et azerty 
Afficher le clip gain line **SHIFT + CONTRÔLE + "-"**  (SHIFT + CTRL + "(" AZERTY)

Avec un clic droit sur l'icône du clip gain : 
Bypass
Clear 
Render 
Ou enlever la line 
Sinon clic droit>Clip gain et on retrouve les meme infos sauf qu'il y a le **copy** en plus. 

Menu>clip>clip gain il n'y aura que le bypass ou le render 

Je peux faire du clip gain avec : 
Le pencil 
Le grabber en créant de break point 

Quand on sélectionne un clip en entier ou partiellement, on peut faire du clip gain nudge quand on fait **SHIFT + CTRL + flèche du haut ou du bas ou avec la molette**  
Les valeur du clip gain nudge se changer dans les preference onglet editing 

Clip gain nodge horizontale (réglable directement dans le transporteur)
**SHIFT + CTRL - ou + du num pad**  on peut aussi utiliser le SHIFT + CTRL "." Et la SHIFT + CTRL "," 
**SHIFT + CTRL + :** et **SHIFT + CTRL + ;** en azerty 
Toujours avec SHIFT + CTRL 

C'est utile pour clean et lisser avant d'entrer dans l'étage de compression 
### groupe de clip 

Dans les groupes de clip si on fait un clip gain sur le groupe, il disparaît si on dégroupe. 
Il revient si on re-groupe 
Le clip gain reste actif tant que le groupe est activé

## Élastique audio 

Pour l'activer on va devoir mettre un plugin d'élastique audio. Il se met dans le header de notre piste. 
On peut le gérer que dans la fenêtre d'édit 

Il y a **6** plugins d'élastique audio 
5 qui fonctionnent en temps reel 
1 x-for qui est forcément en encapsulage 

Pour les temps reel 
Polyrythmic - rhythmic - monophonic - élastiquePRO → Ne change pas le pitch 
Vari-speed modifie le pitch 


Quand on met un plug elastic audio, quand la piste est grisée elle est analysée et donc inutilisable le temps du calcul. 

Il est en reel time car le carrée à coté est vert. Sinon avec X-for il devient gris. 

Les autres peuvent aussi en encapsule 
**CTRL + CMD + Clic** sur le plugin AE on peut les passer en encapsulage ou en temps reel. 

En elastic audio on a deux vues : 
- Analyse 
- Warp 

### Vue Analyse
Les traits en vue d'analyse sont des events marker. S'il n'y a rien en haut et en bas, c'est juste un trait alors on est sur un event marker. 

Il va placer un event à chaque fois que PT considère qu'il y a une transitoire. 

On peut en ajouter : 
- avec le pencil - Clic 
- Avec le grabber - Double clic ou CTRL - Clic 
- Ou clic droit > Add event marker.  Attention cela le place là ou il y avait le sélecteur 
On peut les déplacer sans que cela déforme le fichier. 
Pour les enlever : 
- pencil → ALT + Clic 
- Grabber → ALT + Clic
- Grabber → Double clic 
- Clic droit sur l'évent > Remove event marker  
Pour en enlever plusieurs : 
- on les sélectionne et on fait delete 
### Vue Warp
EN vue de warp on voie les events marker. Mais on a pas la main dessus. 

On peut créer des warp markers. 

Meme chose que pour les events 
On peut en ajouter : 
- avec le pencil - Clic 
- Avec le grabber - Double clic ou CTRL - Clic 
- Ou clic droit > Add warp marker.  Attention cela le place là ou il y avait le sélecteur 
Pour les enlever : 
- pencil → ALT + Clic 
- Grabber → ALT + Clic
- Grabber → Double clic 
- Clic droit sur l'évent > Remove warp marker  
Pour en enlever plusieurs : 
- on les sélectionne et on fait delete

Les warp marker ont un petit triangle bleu en bas du trait

Si on déplace un warp, cela va déformer le signal

### Quantize 

ALT + 0 numpad 

Il va falloir une manipe, il faudra la convertir de sample a ticks. 
Si on applique la quantize il va utiliser les event marker et placer un warp marker dessus. Il fera en sorte de placer ensuite ces markers sur la grille 
Si on ne met pas élastique audio event il ne prendra que le debut du clip et pas les event marker. 
Donc Audio clip ≠ de elastic audio dans cette fenêtre. 

Indicateur de modification par elastic-audio petit entonnoir en haut à droite du clip. 


# Chapitre 6 

## Import 
Plusieurs manières de faire des imports 

Fenêtre audio **SHIFT + CMD + I**
On peut drag and drop depuis le finder ou workspace 
On peut drag and drop dans une piste, ou hors d'une piste et cela créera une nouvelle piste. 

**SHIFT drag & drop** forcera a importer sur une nouvelle piste

On peut en importer un ou plusieurs. 
Si les fichiers n'ont pas la meme Fréquence d'échantillonnage il les convertira. 
Si les fichiers ne sont pas du aiff ou du wave les fichiers seront convertit 

Export de fichiers brute 
**SHIFT + CMD + K** ou menu clip list > Export clip as file
Permet d'exporter les fichiers brutes ! Il ne prendra pas les modification d'élasticité audio. 
Si on veut exporter avec les modifie il faut d'abord les consolider. 

Attention cela ne garde pas la synchro, pour garder une synchro, il faut consolider pour que tous les fichiers aient la meme longueur (Ou le meme debut)

La destination par défaut c'est audio files 
Changer pour un dossier qu'on appelle comme on veut (Tapes par exemple) 
Cela permet d'avoir un dossier avec directement les exports. 

### Workspace 
ALT + I ou Menu > Window > Workspace 

Sound library donne accès à des tags de recherches. 
**ALT + clic** sur le tag bleu il devient gris, il n'est plus pris en compte dans mla recherche des fichiers.  Même manipe pour le refaire devenir bleu 

Les dossiers sont gris, cela signifie qu'ils sont physiquement dans la sound librairie 

Sur un dossier bleu c'est qu'il n'est pas physiquement dans la sound library. (C'est un alias)
On peut ajouter des dossier en faisant clic droit dessus > Add to sound library. 
Idem pour l'enlever (Remove)

### Template 

Créer des sessions et les transformer en template → Save session as template 
Cela peut inclure les médias ! 

On peut importer les datas par **SHIFT + ALT + I** 
Menu file import > Session data. 
On a juste à choisir un .ptx 
Cette session nous donne les infos de la session source. 

Force target force la conversion vers le format de la session meme si pas besoin. 

Consolidate prendra que le fichier audio et pas le whole file. 

On peut tenter le match track pour voir s'il y a des pistes correspondantes. 
On peut ensuite choisir les options de session que l'on veut importer. 

Penser à cliquer sur track data import pour choisir ce qu'on veut que PT import dans les différentes track. 

Dans le workspace on peut aussi aller choisir des templates 
Document>pt>Session template 

SI on prend le .ptx et qu'on le drag & drop dans la track list cela ouvrira la fenêtres d'import session data. 

# Chapitre 7 

## Trim 

Trim tool = F6 
Qvec outil commande focus 
Trimmer du debut du clip start to insertion  "**A**" en qwerty et "**Q**" pour azerty 
"**S**" pour trim end to selection 
**CMD + T** = trim to selection 

Trim loop permet de faire du clip looping 

Trim TCE → time stretch, on peut régler les paramètre du time strech dans preference > processing > TC/E 

Trim scrub que pour les protools ultimate 

Si on a trim loop un clip et qu'on reprend le trim standard il va basculer automatiquement sur le trim loop

## Grabber 

Grabber time qui permet que de prendre des sélections continues et les déplacer 

Grabber separation => Permet de séparer la selection dans un nouveau clip. 

Grabber object : Permet de sélectionner deux fichiers sans sélectionner les objets intermédiaires. 

Le ALT permet de dupliquer ce qu'on selection 

## Outils reversible 
Alt permet de reverse 
- zoomer 
- Pencil 
- Trim tool 
On peut inverser leur effet avec la touche alt
## Sélecteur 

SHIFT + Slash (pavé numerique pour azerty) permet d'activer le link timeline and edit selection 5

Quand il est désactiver il y a deux zones dans la timeline. On peut passer de l'une à l'autre 
"$[$ " en qwerty et ^ en azerty pour la zone d'edit sélectionné et ] ($) pour la zone dans la timeline 

CTRL + CMD + P  dynamique transport 
Active automatiquement la lecture en boucle et désactiver link timeline and selection 
Permet de faire commencer sur le playstart marker quand on fait barre d'espace. Il peut être déplacer pendant la lecture 

Efficace pour comparer des debuts de refrains aux autres. 
On pour faire des boucles efficacement.

## Fades 

**CMD + F** fera soit un fade in out ou cross fade 

Capacité d'avoir 5 presets de bases plus on peut aussi les saves dans la machine ou dans la session. 

Le Smart tool permet de faire des fades. L'icône sont seulement 
Les fades du smart tool sont automatiques setup>preferences>editing 
Le changement n'est pas retro-actif 
On peut changer manuellement le fade avec le smart tool 
Setup>preference>editing > Smart tool fade d'ajustement : On peut demander de le faire avec CMD ou sans 

On peut faire des batch fades CMD + F et on configurera la fenetre globale de batch fade. 

On peut demander d'ajuster seulement la pente ou seulement la pente. 
On peut aussi demander a PT de refaire tous les fades. 

Pré-splice pour les pistes de drums comme ca le cross fade se décale vers la gauche et ne bouffe pas le signal 
A l'inverse pour des whoosh on va utiliser le presplice pour ne pas bouffer la fin du whoosh ou du rivert-crash. 

## Groupes 
Les types de groupes : de mix, d'edit et de mix/edit

### groupes de pistes 

CMD + G permet de créer un groupe de piste 
Tout peut être changer sauf l'ID du groupe. 
Maximum de 104 groupe par sessions reparti en 4 bandes de 26 
#### de edit

Quand je change de taille de piste cela change pour toutes les pistes 
Change de vue → sur toutes 
Duppliquer → sur toutes 
#### De mix 
Seules les groupe de mix ou edit/mix on attribute 

#### Global 
Permet de choisir le comportement basic pour tous les groupes. 
Penser à décocher follow global 

### Gestion de groupe 
Groupe surlignés en bleu = groupe actif 
Lorsque le groupe est inactif les pistes deviennent indépendantes. 

On ne peut **pas effacer** le groupe ALL. 
Le groupe < ALL > prend la main sur n'importe quel groupe activé

## Playlist 

Pour revenir a une playliste supérieure 
**SHIFT + Flèche du haut ou bas** = rotation des playlistes de la pistes 

Par défaut la main playlist est par défaut la target playlist 
Quand on fait solo sur une alternate playlist on entendra l'alternate playlist avec l'ensemble des pistes. 

Pour écouter une playlist seule il faut aussi mettre un solo sur la piste principale. 

Pour faire le composite, on va copier un bout sélectionné vers la target playlist : 
- soit on utilise la flèche a droite du solo. 
- **SHIFT + ALT + Flèche du haut** 
- Menu > vEdit > copy selection to > Target playlist 
On effectue notre composite comme ça 

# Chapitre 8  MIDI 

Deux pistes peuvent gérer du midi : 
- Instrument et MIDI 
Dans les pistes midi il y a seulement des informations midi. 

Le bouton Automation lane permet de montrer différents paramètres sur la piste. 

**ALT + L** → enregistrement en loop 
**SHIFT + CMD + L** = Lecture en boucle  
On se retrouve dans le meme concept quand audio 
Peut importe ou on s'arrête le fichier prendra la taille de la selection 

On peut activer le loop playback with midi merge 
Dans les option midi du transporteur. Ou 9numpad
Il faut activer la lecture en boucle 

Rec en boucle standard efface à chaque debut de la boucle 

Quand la loop est en midi playback, on est en mode MPC. Le fichier sera la somme de tous les recs. 

Pour avoir du son verifier qu'on a bien le midi thru enclenché : Menu > Option > midi thru 

Alt + clic sur la clip list sur un fichier midi. 
Setup > Préf > MIDI on va pouvoir voir le default thru instrument : 
- on peut choisir ce qui va servir a lire le fichier. 
- First selected midi track 

## MIDI Editor 

MIDI Editor window : **CTRL + =** 
Docked midi editor : **SHIFT CTRL ALT =**

Les deux fenetre de midi sont independantes en termes de sélection d'outis. Elles sont strictement indépendantes. 

Dans la track view du midi window : On voit seulement les pistes midi ou instrument. 

Les solos mutes et rec sont appliqués sur les pistes affichées. On peut le voir dans la track list avec le petit rond indiquant shown track ou hidden track. 

En cliquant sur la notation display cela le transforme en partition. 
Annotation display 

On peut avoir plusieurs fenetre de midi editor dans une meme session. Le crayon dans la track list nous indique ou on programme.  On peut le mettre sur plusieurs pistes en faisant **SHIFT + Clic** dans la track list du midi editor. 
Le déplacement s'applique seulement sur la piste sélectionnée. 

On peut se repérer grace au codage par couleur par piste ou par vélocité en au du piano roll. Deux icônes 
Soit on affiche les couleur des tracks 
Soit on affiche l'intensité de la couleur en fonction de la vélocité. 

SHIFT CTRL CMD $[$ m 

SHIFT CMD $[// ]$ zoom uniquement des fichiers midi 

Menu > event > remove duplicate notes. 

Pour se déplacer dans la fenetre : 
- flèche de droite ou de gauche 
- Quand tab to transient → Tab ou alt-tab pour revenir.  (CTRL + TAB win)

Transposer une note : 
- demi ton par demi ton : flèche du haut ou flèche du bas. 
- Par octave : SHIFT + flèche du haut/bas

Transposer en fonction de la tonalité programmée dans la ruler de key. 
- CTRL + Flèche du haut/bas : prendra que les notes de la tonalité 

SI on rajoute ALT à n'importe quel de ces trois cela copie la note 
Si on en a mare d'entendre le son quand on édite. On décoche l'aspect midi sur le transporteur icône à coté du haut-parleur. Penser de le réactiver quand on rec. 

Convertir le midi en audio. 

On sélectionne les clip et on les drag and drop sur une piste qui a le meme format.\

Convertir de l'audio en midi : 
Pareil on prend de l'audio que l'on drag sur une piste midi. Ensuite on choisit l'algorithme. 
Ou clic droit sur le clip audio > Extract midi to new track 
Ou menu > track > extract midi to new track 

Pour le percussifs cela marche bien pour le reste pas ouf. 
Un signal riche en harmonie on préférera le programme : universel (meilleur pour les signaux complexe)

# notes

**CTRL + ALT + CMD + flèche du bas**  → Affiche toutes les pistes dans la fenêtres d'edit 

**CTRL + CMD + flèche du bas** affiche que les pistes du curseur → affiche les pistes sur lequel le curseur est en plein écran. 

Saturator :
Chez [[Plugin Alliance]] 
[[Black box hg2]] 
[[VSM-3]]