---
Matière: Protools
Semestre: B1-2
Date: 2023-10-11
Prof: Alexandre Badagee
Type: notes de cours
---
# Certification Protools
Date: 2022-05 | Tags : #cours 
# CHAPITRE 1 : Quelques bases

## Freq d’ech, bitrate bases des fichiers audio

Les types de forme : Sinus, carré, triangle, dents de scie

La fréquence fait référence au pitch du signal

bande passante oreille humaine 20-20000Hz

Amplitude ce mesure en dB

Conversion PSM (pulse code modulation)

sample rate = nombre d’échantilon par seconde : filltre de shannon = fc = mini 2fc

A 44100Hz dernière fréquence enregistrées = 22050 au delà elles subiront un effet d’aliasing.

Bitdepth = codage de la dynamique de l’enregistrement. Avec 6db/bits, 24 bits = 144dB

### valeur en bits

En 16bits = 65 536 nombres de valeurs

24Bits = 16 777 216

32bits = 4 294 967 296

plus le bitdepth est grand plus on va avoir de poids de fichier.

Calcul de poids de fichier = nb canaux x nombre d’octets (=8bits) x Freq D’ech x Temps en seconde

Etalon : mono 16bit 44.1kHz x 60 = 5167870 Byte = 5Mo

double un de ces paramètres = double du poids

je passe de 16bits à 24bits je multipli par 1,5

## Plus de détails sur Pro tools

DAW = Digital audio workstation 

création  = Digidesign maintenant c’est Aviid

Deux configuration possible : Project = cloud, une session est en local sur l’ordi.

Wholes files et subset clips

file existe physiquement sur votre ordinateur, un clip ou subset clip c’est une entité crée par protools pour les besoins de la session.

prottols et tous les editeurs audio : Editeur audio dit non linéaire, ils sont non-destructifs.

PT permettra de faire des processing en real time ou des processing en encapsulage (rendering)

PT existe en trois version artist, studio et Ultimate 

**Artiste :** 16 I et 16 out simultané, 3 projects simultanément dans le cloud, format de fichier stéréo max, 4go de RAM minimum, 8 recommandé

**Studio :** 64 In et 64 Out simultané, nombres de projets illimités, gestion du nombre de canaux illimié (depuis l’année dernière) 16go de RAM minimim 32 recommandés

**Ultimate :** nombre I/O disponible simultanément 256 in et 256 out, nb project = illimités, nb de canaux par voix = illimité

Nombres de projects sont plus ou moins limités

- MAC/WINDOWS : Question équivalence des raccourcis clavier
    
    Ctrl mac = Start de windows
    
    CMD mac = ctrl win
    
    Opt mac = ALt win
    
    shift mac = Shiflt win
    
    Return Mac = enter win
    
    attention ne pas changer les raccourcis claviers (les mêmes depuis des années)
    

CPU : Central Processing Unit

Logiciel dis natifs on va etre sur le calcul du CPU, contrairement à protools ultimate qui est géré par le DSP de l’interface Protools (digital signal processing)

Random Acces Memory = RAM 

Les sessions doivent etres mises sur un ssd sinon sur Hdd il faut qu’il tourne à 7200tr/min

Entrées analogiques :

Mic

Line 

DI

Entrées Numériques

AES-EBU 

ADAT

SPDIF

### systèmes de monitoring :

Headphones (closeback, semi-open back et closed back)

prise son = closeback, mix = open back

### Installation du protools :

Crée un compte Ilock

crée un compte aviid, qu’on va lié au compte Ilock, pour qu’il puisse téléverser notre licence dessus.

Le système Ilock est basé sur la technologie d’autorisation PACE

Quand on achete notre licence on obtient une carte qui génére une licence téléversé dans notre compte ilock

Les installeurs disponible sont dans notre compte avid. 

Avid link s’installe automatiquement avec protools. 

Protools s’installe avec un tas de plugins : bundle d’air 

# CHAPITRE 2 : L’interface du logiciel

On allume les moniteurs en dernier 

On les éteint également en premier quand on arrête

Quel est l’équipement qui est allumé en dernier dans un système ? Les moniteurs 

Je peux aller chercher les cession récentes avec le Dashboard.

Open from disk = chercher n’importe quelle session 

[CMD O] ou menu file-Open

[SHIFT CMD O] = dernière session ouverte qui va s’ouvrir.

Setup-Playback Engine - permet de controler quel moteur de lecture va ouvrir la session

si une session est ouverte PT va sauvegarder, fermer et réouvrir la session une fois le playback engine mise à jour. 

Pour utiliser plusieurs cartes son : Il faudra choisir le moteur de lecture PT aggregate IO (deux cartes son 8-8 = une carte son 16-16)

Sur mac on peut bosser avec le moteur de lecture de mac

Hardware setup- Lauch setup app = on sort de protools - ouvre la configuration audio du moteur de lecture choisis (on peut gerer le pt aggregate ici)

dans la session deux fenêtres : EDIT et MIX

keyboard shortcut : follow keyboard layout pour les azerty sur windows

Fenetre de mix [CMD 1] / menu window = fenêtre de transport.

à l’arret on a l’edit cursor quand ça joue c’est le playback cursor

return to 0 = return | got to end = ALT + return
fast foward/rewind avec le 1 et 2 du Numpad

[CMD S] ou menu-file-save, on sauvegarde sous le même nom de session

[CTRL CMD S] = save as, on change le nom de la session et on se retrouve sur la nouvelle session qu’on vient d’enregistrer.

Sortir de la session ce n’est pas fermer les fenêtres.

pour soritr de la session il faut faire SHIFT CMD W ou menu - file -close session.

CMD Q on quitte protools, on est dans l’OS

crée une session CMD N ou menu-file-session

On ne peut pas utiliser de caractères ASCII asc2 sur les noms de session (caracter illegal)

Session c’est sur notre disk dur 

### Création session

différence entre aiff ou Wave 

AIFF : pas la possibilié de travailler avec le timecode (on enregistre jamais en musique à l’image ou en post prod en aiff)

BWF (WAVE) :  broadcast wave file (il a la capacité d’encapsuler des métadata sur le fichier notamment le timecode).

Ce sont les suls formats disponible.

La Freq d’ech est en fonction de la carte son utilisée.

I/O setting gestion des entrées sorties de l’interface audio : soit on fait notre mode personnel ou alors on va utiliser Stéréo Mix. (on utilise le last Use que si on est certain que la session va ressembler à elle juste avant (pour un album par exemple)

Interleaved = entrelacés vs séparation des canaux.

capacité de crée des sessions à partir d’un template. 

- ça crée un dossier racine dnas lequel il y a :
    
    des fichiers : 
    
    - le protools session file (pour les version antérieur à protools 10, .ptf : pt7 à 9, .pts de PT 1 à 5) : .ptx
    - wavecachefile (il enregistre les informations de formes d’onde de nos fichiers audios, si il est supprimé, il sera recrée à l’ouverture de la session
    
    des sous dossier
    
    - Audio File : seules les wholes files se trouveront dans le dossier audio file de ma session (soit en .wav ou .aiff en fonction du choix)
    - Bounce File : (contient tous les fichiers ici de la fonction bounce mix ou track bounce)
    - Rendered FIle : tous les ficheirs issus de la fonctions elastique audio ou rendering seront dans ce sous dossiers
    - Clip groupe : tous les groupes de clip seront exportés dans le subfodler clip group
    - Session File Backup : toutes les sauvegardes automatiques : nom de session.bak000.ptx (il peut y en avoir 999 espacé minimun d’une minute)
    - Vidéo Files : localisation du dossier dans lequel il faudra mettre manuellement la vidéo avant de l’importer.
    

Dans la session la barre d’outil supèrieur c’est : la toolbar 

### La ToolBar

tout a gauche : Edition mode 

Edit tool : zoom toggle zoomer tool, trim,Selecteur,  grabber ,scrubber , pencil

dessuos edit tool dans lordre : 

Tab to transient 

Link timeline and edit selection

Link track and edit selection

Insertion follows playback

automation follows edit

mirror midi editing

layering editing (permet d’editer en chevauchant les clip)

main compter et un sub compter

start, end et length on obligatoirement la même unité que le main compteur

Rapport de grille et nudge (petits déplacements) les valeurs de ces deux sont totalement indépendant (dans l’unité et la valeur temporelle)

module concernant la métrique et la barre de transport.

CMD plus prendre le module et le déplacer ou on veut sur la tool bar

L’ensemble des sous menus sont diponible dans le mune en haut à droite de la toolbar

### Les rulers

ils sont réordonnables pour convenir à notre utilisation

les timeline rulers : conducteur de temps

les commande rulers : conductor rulers

de part et d’autre de la fenêtre d’edit on a track list et clip list : apparition de l’ensemble des piste meme si elles sont cachées ou inactive

groupe list

clip list (attention ici on va voir les fichier avec pt artist et studio audio, midi et group de clip, pt ultimate clip audio midi groupe de clip et aussi les clips vidéos)

### Fenetre de mix CMD =

on retrouve la trak,group list

la clip list n’apparait pas dans la fenetre mix

la piste vidéo n’apparaitra **jamais** dans la fenetre de mix

dans la fenetre de mix et qu’il y a beaucoup trop de piste ALT CMD M menu -view narrow mix (une seule taille possible) cela permet d’avoir une visualisation de plus d’éléments

CMD 1 ou menu-window-transport fenetre de transport 

en double écran permet d’avoir les informations de timeline sur la fenêtre de mix (elle est réarrangeable)

### Fenetre d’edit

elle est configurable dans le menu-view 

menu-view-ruler equivalent de clic sur l’icone du menu de la timeline, ou clic droit sur le nom du ruler (bar|beats, timecode etc…)

menu-view-edit window view ou clic droit sur le nom au dessus des pistes

alt clic dans ses deux fenetres masque ce sur quoi tu clic (les sends une timeline etc…)

CMD K active ou désactive le préroll

### Menu de protools :

- File

création sauvegarde, export, import audio/video 

- Edit

edition simple ou avancé 

View

affichage ou masquage

Track 

tout ce qui est en lien avec les pistes

Clip

Tout ce qui est en lien avec les clips

Event

Tout ce qui est de l’ordre du MIDI c’est dans event

Audiosuite

menu d’encapsulage : on y retrouve tous les effets disponible pour la fonction audiosuite

Option 

option de lecture d’enregistrement, de solo (On/off de base, 

Setup 

ordre de la configuration du hard ware de la carte son. C’est un menu a dialog box, il ouvre tout le temps des fenetres

Window

gestion et affichage des fenetres principales et flottantes

Avidlik

Acces à des fonctionnalités de avid link dans protool

Help

Documentation et raccourcis protools, on peut taper une requete et trouver les articles qui traite de ce sujet la 

# CHAPITRE 3 : pistes, workspace et preview

## Les pistes en fonction des versionq

| Type de piste | Nombre max PT Artist | Nombre max PT Studio | Nombre max PT Ultimate |
| --- | --- | --- | --- |
| audio | 32 mono ou sté | 512 mono sté multi | 2048 m,st,multi |
| aux input | 32 mono ou sté | 128 | 1024 |
| Midi | 64 | 1024 | 1024 |
| Instrument | 32 mono ou sté | 512 | 512 |
| Master Fader | 1 mono ou sté | 64 | 1024 |
| Video | 0 | 1 | 64 |
| VCA | 0 | 128 | 128 |
| Folder (basic) | 2000 | 2000 | 2000 |
| Folder (routing) | idem aux | idem aux | idem aux |

### Différent type de piste :

- Pistes audios :
    - PT artist : 32 pistes mono ou stéréo
    - PT studio : 512 piste mono, stéréo (piste 5.1 sera équivalent à 6 pistes mono/ 3 piste stéréo)
    - PT ultimate : 2048 pistes mono, stéréo, multicanales
- Aux input :
    - PT Artist 32
    - PT Studio : 128 mono, stéréo ou multicanal
    - PT Ultimate : 1024 m,st,multi
    
    elle ne contient aucun clip
    
- Piste MIDI
    - PT artiste : 64 Piste
    - Pt studio et ultimate : 1024
- Piste Instruments
    - PT Artiste : 32 piste m,st
    - PT studio/ultimate : 512 pistes M ou St
- Master Fader
    - PT artist : 1 master fader mono ou stéréo
    - PT Studio : 64 Master, mo,st ou multi
    - PT ultimate : 512 master fader m,st ou multi
    
    sur une piste master fader il n’y a pas de clip 
    
- Piste Vidéo
    - PT artist ne gère pas la vidéo
    - PT Studio ne gère qu’une piste vidéo
    - PT ultimate peut gerer 64 pistes vidéos mais une seule peut etre en lecture à la fois
- VCA
    - PT artist : ne gère pas les pistes VCA
    - PT studio et ultimate : 128 pistes VCA
    
    Elle ne contient pas de clip
    
- Folder Track
    - Basic = aucun format à choisir.
    - Routing = il faut choisir le format
    - All PT : 2000 basics folder tracks possibles
    - pour le nombre de routing folder track = le même que pour les auxiliaires :

Chaque type de piste à un icône :

### Création de piste

Création de piste Shift CMD N ou Menu-piste-new

- Raccourcis lors de la création de piste :
    - CMD ←/→  changement du format
    - CMD fleche du haut/bas change le type
    - ALT CMD Fleche du jaut/bas Relation de temps
    - Shift CMD fleche du bas pour créer un nouveau type de piste

Quand on crée une multitude de piste c’est pour avoir le même corps en terme de nom et des chiffres juste après celui ci.

Les pistes apparaissent dans l’ordre des lignes des pistes.

Si c’est le bordel dans les I/O il faut aller dans menu→setup→IO setup puis de cliquer sur Default (si c’est le bordel en terme de configuration, ça réinitialise les IO)

### La selection des piste

- La selection des pistes
    
    Sur les pistes : 
    
    - continue : SHIFT + Clic
    - Discontinue : CMD + Clic
    - Selection/déselection de tout : ALT
    
    Dans la track list de l’edit, du mix et sur les track directement
    

On peut cacher des pistes : 

les points à droite du nom des pistes dans la track liste permet de savoir si les piste sont cacher ou pas 

c’est également dans la track list qu’on cache les piste

Les 3 selections fonctionnent aussi pour cacher et décacher les pistes.

- Renommer les pistes
    
    double clic sur la piste à la fin CMD → on passe à la piste suivante : Return pour valider
    
    Clic droit rename ne permet pas de passer aux pistes suivantes. 
    
    Le menu clic droit est le menu propre à la piste sur laquelle on a cliqué.
    

Changer l’ordre des pistes : en drag and drop : sur la track list, la fenetre de mix et d’edit.

Dans la fenetre d’edition on peut changer la taille soit en cliquant sur l’echelle à gauche de la piste soit dans le menu de la piste → track high

CTRL fleche du bas/haut change la taille des pistes sur lequel est le curseur.

Alt applqiue sur toute les pistes et shift alt applique sur les pistes selectionnées.

### Pistes :

Toutes les pistes ont un mute et un solo.

ALT + mute : mute all

ALT + SHIFT + mute = Mute selection

Solo : 

XOR désoloise quand je clic

shift + clic permet de cumuler les solos

LAtch les solo s’ajoutent quand on clic sur le solo d’une nouvelle piste

### Delete

Il faut faire clic droit sur la piste→delete

Ou menu→track→delete

La piste est effacé mais les clips restent dans la clip list.

### Import

Menu-file-import-audio

SHIFT + CMD i

On peut soit :

- Add > ne crée seuelement un alias, un chemin vers le fichier (si le fichiers n’est plus disponible, il n’apparaitra pas)
- Copy > quand on travaille pas sur un serveur (cela crée une copie du fichier dans le dossier de session
- Convert > quand on travaille pas sur un serveur (cela crée une copie du fichier dans le dossier de session
    
    On peut le placer : session start (début) song start (début de chanson), selection (sur le cursor), spot (ouvre la fenetre spot pour savoir ou mettre le fichier)
    

On peut ajouter des média via : le finder ou le workspace

→ il faudra juste drag and drop dans la fenetre édition : 

- crée une piste si drop pas sur une piste
- crée un clip si drop sur un piste existant
- crée rien dans le projet si drop sur la clip list

Par défaut le drag and drop du finder dans la session ne copie pas le ficheir dans la session, pour le forcer on peut :

- appuyer sur ALT lors du drop
- Menu→Setup→preference→processing→automatically copy file on import

### Workspace

ALT + i crée un workspace

pour ramener le workspace devant Alt + J ramene l’ensemble des workspace crée 

ou window→workspace→bring to front

Le workspace contient plusieurs navigateurs : 

- sound library
- Volumes (les différents volumes présents sur la machine)
- navigateur de session : le dossier audio files ne représente pas le fichier physique, il représente l’ensemble des fichiers audio en multi-disque c’est un dossier virtuel
- Catalogues : permet de manipuler des banques de sons
- user : permet de se balader dans la hierarchie de l’ordi sans sortir de protools

on peut faire deux types de recherches : 

- recherche simples CMD + F: on tape un terme qui est scanné par pt et il me donne tous les fichiers qui ont se nom dans leur nom de fichier (il scanne l’ensemble du système)
- recherche avancé SHIFT + CMD + F (loupe avec croix) : on peut faire une recherche plus détaillée :
    - détail sur les noms
    - sur le type
    - le nombre de canaux
    
    on peut choisir ou il effectue la recherche dans la recherche avancée
    

### Preview

Possibilité de faire une preview : Toute lecture qui n’est pas déclencher par la barre d’espace

clic droit sur le bouton play de la preview pour avoir ces options : 

Clic droit sur la preview → on peut mettre la preview en boucle ⇒ Loop preview

Auto-preview : lecture du fichier uniquement en cliquant sur le fichier (on a pas besoin d’appuyer sur le bouton lecture)

Space bar toggle play preview : la barre espace déclenche la preview et pas la lecture du projet.

Audio file conform to session tempo : permet d’écouter une boucle au tempo de la session et pas à son tempo original

ces options sont retrouvables dans le menu du workspace

Pour la preview il faut qu’un audition path dans le IO setup soit actif.

On peut choisir l’endroit ou on veut écouter la preview en cliquant sur l’endroit sur la waveforme de la preview.

# CHAPITRE 4 : Edit

### Les compteurs

l’unité du main compteur :

- Shift cmd clic sur les rulers
- clic droit sur le main compteur

Musique : bar-beats

post-prod : Timecode

Il remplace le ruler de la timeline en fonction du main compteur

- Start, end and lenght : c’est la selection : on peut définir la selection en tapant la valeur et en entrant return pour déterminer la selection (attention il faut valider avant de passer à une autre valeur)

Lecture en boucle : la selection doit au moins faire 0,5 secondes !

SHIFT CMD + N, ou 4numpad ou clic droit sur icône Play ou menu→option→loop playback

### Naviguer dans la session :

scroll verticalement : uniquement mousewheel

scroll verticalement : SHIFT + mousewheel

Zoom : (module de zoom dans la tool bar par incrément en cliquant sur les fleche de par et d’autre des deux icones ou en cliquant et bougeant de gauche à droite pour zoomer de façon linéaire)

Zoom Vertical : ALT CMD crocher qui s’ouvre / ferme (dollar et circonflex) audio et midi sont strictements différents

Zoom horizontal : T ou R, ALT + mousewheel centre la ou est ton curseur.

F5 = zoomer tool : on détermine une zone et il l’affiche / Alt clic ça dé-zoom (on le voit avec le moins sur la loupe)

double clic sur le zoomer tool : PT ramène l’intégralité des clips de la session sur l’écran.

Avec CMD et l’outil permet de faire un zoom verticalement et horizontalement (le zoom de la forme d’onde est inversement proportionnel au mouvement vertical.

ALT A sur les clavier qwerty afficher l’intégralité de l’écran et des formes d’ondes

Selection : centrer la selection sur l’écran ALT F

### Modes de défilements :

Quand on joue de base le playback cursor revient à la position du selection cursor

option→edit window scrolling : 

- no scrolling l’écran reste sur le cursor de selection
- after playback : centre l’écran sur la fin de la zone de lecture (mais ne bouge pas le cursor de selection)
- Page : Déterminer une zone (nombre de mesure/ temporalité) et pt faire faire défiler le projet par incrémentation de cette zone. A l’arret protool garde la fenetre ou le playback c’est arrêté (mais le cursor reste la ou il était)
- Continus (rien sur la partie gauche) : c’est la timeline qui avance et le curseur reste fix, je reste à l’endroit ou je me suis arrêté
- Center Playhead (la barre est bleue et pas noire) : idem la timeline avance et le curseur est fix, mais le curseur est placé la ou la lecture c’est arrêté.
    - Quand on active le insertion follow playback : Le curseur se trouve la ou c’est arrêté la lecture. (le point d’insertion suit la lecture)

### F6 Trim

possibilité de le renverser en appyant sur ALT

### F7 Selecteur

Quand on double clique avec le selecteur, on selectionne la zone en question

Triple clic : ensemble des clips d’une piste

### F8 Grubber

Clic = selection

double clic = renommer

prendre et daplacer le fichier

avec ALT on duplique le fichier

### F9 Scrubber

On peut scrubber que deux pistes maximum par session

Lire à vitesse ralentit (détecter les clip numériques)

### F10 Pencil

Pleins de formes à disposition

En automation pas les curves

En fade/chgmt de tempo pas les changement autres que curves

On peut réécrire la forme d’onde → c’est une action destructive (la modification est directement dans le fichier d’origine)

## Modes d’éditions

- F1 Shuffle :  quand on supprime le vide est enlever. et quand on dupllique il pousse les clip qui viennent après le curseur. (utile quand on fait la map du curseur). Les déplacements ne permettent que de ce coller de bords à bords avec les autres clip.
- F2 Spot : il ouvre une boite de dialogue pour savoir ou sera placé le fichier/le déplacement
- F3 Slip : libre
- F4 Grid : selection et daplacements en fonction de la grille
    - absolu : on place le début du clip sur la grille
    - relative on déplace en incrémentant en fonction de la grille

# CHAPITRE 5 : enregistrement

Alimentation phantom de 9V à 54V

Les deux niveaux à disposition : Niveau pro +4dBu, Niveau grand public -10dBV

Formats audio numériques : 

AES EBU : Audio engineering society - European Broadcast Union

SPDIF :(grand public/semi pro) Sony philips digital interface 

ADAT : les gens ont mis un acronyme

## Le Tempo

default : 120bpm

## Fenêtre de transport

Icône chef d’orchestre c’est le conducteur : il permet de faire des changements de tempo.

sinon sans le conducteur : un seul et unique tempo : on est en manual tempo

En cliquant sur le plus du ruler tempo on peut ajouter un tempo

tap tempo : T après avoir cliquer sur le tempo

## Métrique

défault 4/4

Pour changer de métrique : il faut double cliquer sur la métrique

ou sur le ruler meter on clique sur le +

## Clic

menu-track-click-track

il faut le configurer : 

menu→setup→click/countoff :

- on a trois possibilités :
    - Only During play
    - During record
    - During countoff

pour activer le clic

- menu→option→clic
- 7 numpad
- Sur le bouton de la fenetre de transport (un métronome)

## Piste

quand on renomme la piste ça ne renomme pas le clip

quand on baisse le fader de la piste ne permet pas d’enregistrer le signal moins fort (le fader c’est le niveau d’écoute du fader)

ALT + Clic remet par défaut (unity gain)

checker si on a de la place : menu→window→disk usage 

permet de voir la disponibilité disponible.

Input monitoring on écoute ce qu’il y a en entrée de la piste, quand c’est gris joue ce qu’il y a SUR la piste

Shift I active l’input monitoring

Le rec

pour lancer l’enregistrement : 

- CMD Spacebar
- F12
- 3 numpad

Le fichier se nommera le nom de la piste “_” le numéro de la take

Quand on rec, ce sont des whole file car dans la clip list les fichiers sont en **gras**

Ils seront dans le fichiers audio files de la session

Quand on coupe un fichier il ajoute “-”pour leur nombre, pas en gras car se sont des subset clips.

Impossible d’effacer un whole file dont un des subset clip est présent dans la timeline.

Pour les renommer : double clic avec le grabber. 

On peut les renommer soit sur la session soit sur le disque dur

Automation follow selection → déplacement de l’automation avec le clip ou non?

### Effacer des clips

Dans la clip list

SHIFT CMD B

Dans le menu de la clip list : 

Delete : enleve de la session mais restent sur le disk

Move to trash : Enleve de la session et du disk et les placent dans la corbeille

Remove : enleve de la session et de l’ordi, irrécupérable

PT va demander la validation pour chaque fichier en maitenant ALT on peut valider pour l’ensemble des fichiers

# CHAPITRE 6 : MIDI

MUSICAL INSTRUMENT DIGITAL INTERFACE

C’est un protocol 8 bits. Il ne fait pas de son.

On peut véhiculer jusqu’à 16 canaux par connectique MIDI

Piste MIDI : pour avoir du son il faut lui adjoindre une piste auxiliaire

Piste instrument : “rassemble la piste midi et auxiliaire en une seule piste”

Attention : Sur la piste midi les entrées sorties sont des IO Midi et pas Audio

l’équivalent du midi se trouve dans la partie instrument de la piste instrument.

Si la piste est grisée c’est qu’il y a eu un soucis dans le link MIDI

Les deux vues pricipales : sont :

La vue de clip (on voit les informations midi) → fonctionne comme n’importe quel clip audio ⇒ edition

La vue de note (qui permet de programmer les éléments midi) ⇒ programmation des notes

## Fenêtre de transport

On peut activer le clic countoff avec les icone ou 8 Numpad

Icone avant le clic

Wait for note il lancera l’enregistrement quand il aura une information midi

menu→setup→preference→midi→use f11 blablabla → on peut parametrer que la touche F11 active ou desactive le wait for note

Icone avec les deux fleches : MIDI Merge → Permet d’enregistrer en boucle et d’ajouter l’écriture sur la boucle déjà enregistrée

Midi merge = 9 Numpad

ALT CMD I = Importer du MIDI (.mid) ou File→import→MIDI

Les fichiers midi sont encapsulé dans le Protools session file (.ptx)

Quand on importe on peut importer comme instrument ou en MIDI

On peut choisir si : 

on importe et applique le tempo du midi

on importe la key signature (tonalité)

on peut effacer l’ensemble des piste midi

effacer les pistes instrument

si on a des clips midi on peut tous les effacer

Pour l’enregistrement midi : 

On arme la piste de manière standard. Pour en armer simultanément il faut : SHIFT + clic

F12 / 3 numpad / Spacebar

Je veux faire du midi merge, ce n’est pas l’enregistrement en boucle mais bien la lecture en boucle qu’il faut activer. 

SHIFT K ou Window→midi keyboard permet d’utiliser les touches du clavier pour jouer.

### Instruments Virtuels

- Xpand! : il possède 4 players
- BOOM : programmation de rythmes, c’est une boite à ryhtme
- DB33: simule un son d’orgue
- VACCUM : Synthé à Lampes
- GROOVECELL : MPC
- SYNTHCELL : Synthé programmable
- Structure Free: sampleur livré avec protools

Pour les paramètres et presets : on peut cliquer sur la fenêtres ou sur les deux fenetres ce qui ouvre une fenêtres ou on peut choisir une incrémentation automatique dans la liste des presets. On peut les faire défiler avec le + ou - les presets

Les valeurs sont en Tics : 1 quaternote (note) = 960 tics

Une heighnote(croche) = 480 ticks

Note en midi sont soumisent au modes d’édition (slip, grid, shuffle, spot)

par défaut une piste midi et instru est en tic based.

horloge = sample

metronome = tic

c’est la référence de temps

menu→setup→preference→editing→new tracks default to tic time based

Grabber : double clic → efface

SHIFT CMD crochet qui se fermet. s’ouvrent permet de grossir les piste midi ou isntrument.

Lorsqu’on voit des losanges sur les blocs midi on est sur la vue de vélocité.

Les edti modes et les édits tools fonctionnent

Pencil il se transforme en grabber et trim en fonction de sa position avec la note (sur la note = grabber, sur le coté trim tool)

Si on maintient CMD avec le PENCIL permet de gérer la vélocité de la note (sans switcher sur la vue de vélocité)

SHIFT CTRL CMD crochet qui s’ouvre  (circonflexe)= tout mettre en visu

Sur la piste instrument il y a les automations de la piste et les controle continu.

en controle continu c’est de l’information midi donc on a que 127 valeurs.

Automation de tempo triangle square et random ne sont pas accessible. 

On peut changer le tempo avec Event→time Opération

cut time/add time/change metrics/move songs start

Event→Event opération → options de quantification et de transpositions

Quantification ALT 0

Transposition ALT T

# Raccourcis Bonus

Zoom avec CMD 

CTRL CMD crochet qui s’ouvre equivalant ALT A mais ne remets pas le zoom verticale

CTRL ALT CMD fleche du bas toutes les pistes entrent dans ta session

CTRL CMD Fleche du bas/haut zoom sur la piste selectionnée

CTRL ALT CMD ← / → permet de changer le type d’affichage

CMD virgule place un point de synchro

CONSOLIDER =  SHIFT ALT 3

Tap to to transient → Tab / anti = CMD TAB ou selection → CMD SHIFT TAB / SHIFT TAB

[https://www.notion.so/Certification-Protools-af34837db636418ba957023216ebd2e9?pvs=4](https://www.notion.so/Certification-Protools-af34837db636418ba957023216ebd2e9?pvs=21)

# Chapitre 7 EDITING

Link track to link selection →lors d’une sélection cela sélectionnes mes piste aussi 

Permet de sélectionner les pistes rapidement 

CMD B ou menu→edit→clear : enlever l’element sélectionné

CMD X ou edit→cut cela permet de coller se qu’on vient d’enlever

CMD Z : undo

SHIFT CMD Z : Redo 

les deux se trouvent dans le menu edit

### Dupplication

Grabber + Alt = Dupliquer

CMD D : duplique **la sélection une** et une seule fois

ALT R ou edit→repeat ou on peut choisir le nombre de répétions dans une fenêtre.

### Séparation

On peut séparer une selection 

CMD E ou b ou edit→separate clip at selection : cela désolidarise la selection

edit→separate clip on grid permet de separer le clip à la mesure avec un retard qu’on peut choisir

edit→separate clip at transient : separer les clips à chaque transient. 

Les deux manoeuvres peuvent être réalisés avec un clip séparé et selectionné

CMD H edit→heal separation

Fonctionne que si les fichiers appartiennent au même whole file et qu’ils n’ont pas été déplacés.

Plusieurs fichiers qui n’appartiennent pas au même whole file : on peut les consolider

SHIFT ALT 3 ou edit→consolidate

### Time stretch

quand on appuie deux fois sur F6 on arrive sur le TRIM TCE ce qui permet de faire du time stretch

Permet donc de compresser les fichiers en terme de timing.

algo : setup→preference→processing→TCE on peut choisir l’algorithme qui calculera le TCE

### Loop

Selection du fichier puis clip→Loop file ou ALT CMD L

permet de choisir le nombre de boucle :

- en fonction du temps
- en fonction du nombre de mesures
- à la fin de la session ou jusqu’au prochain clip

Il y a une petite flèche qui indique la boucle

Avec le trim loop F6, si on trime le fichier, PT va looper le fichier selectionné.

En maintenant Ctrl avec le trim loop permet de faire des boucles entières

### Nudge

il est sous le grid, il est indépendant de lui. Il fonctionne dans n’importe quel mode d’édition.

Avec les touches  + et - du numpad 

ou ; et : sur azerty ou , et . sur qwerty.

### fade/crossfade

Selection puis : 

CMD F ou edit→fade ouvre une fenêtre qui permet d’ajuster et d’écouter le fade.

Setup→préference→editing on peut regler la taille par défault des fades et la zone d’écoute des fades.

Dans la fenêtre on peut choisir ce que l’on voit :

- permet de voir juste les courbes
- juste les courbes
- comment elles se melent
- comment elle fusionnent entre elles : si une fréquence ce crée, on va voir une fréquence se crée au milieu du crossfade.

Il faut vérifier en terme de in ou out la sommation. Quand on est sur on peut valider le fade. 

Il n’est pas définitif. on peut l’éditer après sa création.

Link in/out : 

- Equal power : réaction logarithmique pour les signaux non-phase coherent (choix premier) j’écoute si ça ne marche pas alors on se met en equal gain
- Equal gain cross fade linéaire, pour les fichiers phase coherent
- none permet de décaler le début et la fin d’un fade in ou d’un fade out

D ou G permet de faire des fades automatiques avec le selecteur à l’intérieur de la sélection. 

Ctrl G ou D ou F, si pas l’outil command focus d’activé. 

Avec F même chose mais il faut une sélection. 

Clic droit sur un fade permet certaines options de la fenêtre

on peut aussi delete le fade avec le clic droit.

**Batch fade**

CMD F sur une selection permet de choisir lles pentes des trois types de fades et de choisir comment il crée les fade et si PT ajuste les fades existants.

On peut demander un placement précis des crossfades : 

elements transitifs : pre-splice

Sinon on utilsie les autres

### Déplacement

Tab 

quand tab est activé sur windows. L’option de mac devient le CTRL du windows

Quand le tab to transient n’est pas activé. Il permet de se déplacer de bord en bord dans la session

Tab vers la droite ALT tab Vers la gauche

SHIFT TAB selection vers la droit SHIFT ALT TAB selection vers la gauche

Quand l’option tab to trasient est activé CMD ALT TAB 

Permet le même déplacement mais de transitoire en transitoire. 

### PISTE VIDEO

PT STUDIO editing de la piste vidéo impossible

PT ULTIMATE editing de la video possible

Quand on ne bosse pas de vidéo, il faut enlever le moteur vidéo car même si il n’y a pas de vidéo il prend de la ressource

Afficher la video → CMD 9 ou window→video : fenetre d’affichage de la vidéo, on peut changer sa taille en faisant clic droit.

CMD 7 c’est quand on a plusieurs vidéos permet d’aller d’un fichier à un autre sans avoir à dézoommer de la timeline (équivalent de l’univers audio au dessus des rulers)

clic droit sur la piste vidéo permet d’importer le fichier audio de la video dans audio files.

2 vues principales de la pistes : Block ou frame

Quand le moteur vidéo est fragile préférer la vue block.

### Enlever silences

CMD U edit→slip silence enlève les silences

# CHAPITRE 8 : mixage

Le mixage fait référence au mix in the box (à la différence du mix in the box)

Ramener un bouton à sa valeur par défaut/ valeur unitaire → ALT Clic

présicion dnas le déplacement d’un paramêtre : CMD et déplacement avec la souris → Fine Tune : le paramètre va se déplacer avec la plus petite échelle possible.

### Elements centraux d’un mix

kick 

snare

bass

Lead Vox

### Signal Flow

Sur la fenetre de mixage : 

le signal arrive par le haut il traverse la chaine d’insert (les inserts sont pré fader)

après le signal traverse les sends (les sends sont pré ou post fader, et post inserts), possède un panoramique indépendant.

ensuite le signal traverse le fader 

puis le panoramique

et finalement la sortie de la piste.

master fader : les inserts sont post fader (si je baisse le fader, la quantité de signal qui rentre dans les inserts diminue)

### Automation

Quand on mix on fait des automations.

Sinon on fait des mix “statique”

automation de base en mode Read

Mode d’automation : 

- OFF : interdit la lecture et l’écriture des automations
- Read :

### Clip

Quand le master fader est rouge : le signal est au dessus de 0dBFS 

Si on export le signal sera saturé

Si notre signal est saturé sur une piste on peut baisser le master et le signal de sortie ne sera pas saturé (ne marche seulement en 32 bits)

Orange on est en Over 0, le rouge on est en clip

### Aux lié directement au pistes

option solo in place pour les auxiliaire

solo gris : solo safe CMD + clic

version 2023 met les sous groupe en solo safe. 

selection les piste 

SHIFT ALT → clic sur la sortie →new track il va demander la création d’un auxilaire (avec le solo safe)

### Master fader

il peut controler des bus physiques, mais aussi des bus internes. (output bus or internal bus)

Le master fader est en over → il sature dont soit on baisse les individualités, soit on baisse le master fader. 

il peut donc controler des bus internes (sub mix, envoie de delay, reverb)

Il permet de controler le niveau des bus interne. 

Changer echelle de valeur : clic droit → echelle (RMS ou K20)

setup→préférences→metering : décocher track and master type linked

### volume

quand on baisse, cela un impact.

peut importe ou on baisse on n’a jamais le même résultat entre baisser le master fader ou les tracks en individuelles. 

# Chapitre 9

## Effets

ordre des inserts à un impact sur le résultat final.

On a un maximum de 10 inserts par piste maximum

deux types : logiciels ou hardware insert

Quand on ouvre un insert la fenetre est targeté. Si on ouvre une deuxieme fenetre , la 1er se ferme.

Il faut donc soit détargeté la fenetre, soit on appuie sur shift pour ouvrir le deuxième insert.

Avec ALT on peut les copiers sur de nouveaux inserts.

CMD clic  ou clic droit bypas  : BYPASS les plugins (attention ils sont toujours calculés par la machine) (bleuté)

CTRL CMD désactive le plugin (grisé) l’effet ne prend plus de ressources au protools

### Format plugin

AAX : Avid Audio eXtension

C’est un processing real time.

### Sur une fenêtre d’effets

on peut se déplacer dans les insert avec le menu en haut à gauche de la fenetre de plug : nom de la piste et niveau d’insert.

On peut comparer 

Chercher des presets comme vu avec expand!

On peut enregistrer nos présets avec le rond et la fleche à droite des presets

lieux d’enregistrement peut etre choisit en bas du menu dépliant.

### Catégorie de plugin

Sur une piste stéréo : dux catégories de plugin 

multi : droite gauche identiques.

multi mono : la gauche et la droite peuvent etre traité différement (de base c’est linké, quand on relink on détermine le canal maitre)

Il y a des plugins Native. Seuls les Protools ultimate avec carte HDX permettent d’avoir marqué DSP ou les plugins sont calculés par ces cartes)

C’est un protools avec un interface carbon

### EQ

paraétrique / graphique

Equalisation soustractive ⇒ nettoie les surpression auditives

equalisation additive ⇒ mettre en forme la balance tonale

### Dynamique

Pour savoir si un signal est plus compressé, regarder les paramêtres….

Dyn3 est le compresseur de base de Protool : (compresseur, limiteur, expandeur, gate)

### Les sends

Par défaut ils sont en post fader.

L’ordre n’a pas d’impact sur le signal

Pré la fleche est bleue, post la fleche est grise

Par défaut on est sur une ue de send fermés, pour afficher la expanded view → CMD clic sur la fleche ou view→expanded sends

La fenetre de sends est également targétée donc les même manipulations sont disponibles.

Pour naviguer entre les sends on peut utiliser le menu dépliant en haut du sends

par défaut les sends on un pan dédié, FLP follow lead pan → le pan du send sera identique à celui de la piste.

On peut les déplacer, et les coier avec ALT 

Les sends pre fader = circuit de casque

Les sends post fader = Envoies vers des effets

### REVERB

Algorithme de rev 

- room
- chamber
- hall
- church
- plate
- spring

Attention convolution c’est une catégorie de reverb

Pré delay : permet de mettre de la distance dans le mix (plus il y a de pre delay + c’est loin)

### Audiosuite

Traitement audio en encapsulage (rendering)

La différence entre audio suite et real time se fait au niveau du footer avec la possibilité de preview

Et de Render. 

Sous elle menu dépliant jai 4 éléments réglable.

1. pour la gestion du fichier  (destructif ou non)
2. est ce que je layer ou est ce que je l’envoie dans la clip list (USE IN PLAYLIST)
3. Niveau sont analysés : clip par clip ou au niveau de la sommation totale (utile pour la gestion de la dynamique)

Autre option pour encapsuler : COMMIT

Audio suite c’est un menu dédié.

### Automation

Dans le track iew selector ⇒ permet de visualiser une seule automation 

Vs l’icone en bas à gauche qui permet de visionner plusieurs playlists d’automation simultanément.

(attention Les controle continu des pistes MIDI fonctionnent de la même façon mais on aura pas du tout le même rendu)

On peut programmer des automations avec le pensil

La fréquance du pencilest basé sur la valeur du grid ⇒ periode également taille du grid

n peut utilise tout sauf ce qu’on peut utiliser pour programmer le tempo.

On peut gerer la dynamique des courbes en fonctions de la hauteur qu’on trace avec le pencil

On peut trimer uniquement la selection de l’automation avec l’outil TRIM

Le GRABBER permet de crée des points ou effacer des points

On ne peut pas LOCKER de point sur la timeline, on ne peut pas les verrouiller

### Modes d’automation

Write : lecture cela écris l’automation, quand j’arrete la lecture je reviens à la valeur initiale avec un automate time de 0

Latch : je rentre en automation que quand je modifie le paramêtre,, quand j’arrete la lecture je reviens à la valeur initiale avec un automate time de 0

Touch : je rentre en automation que quand je modifie le paramêtre, quand j’arrete la lecture je reviens à la valeur initiale avec un automate time choisis  Setup→preférence→mixing automatch time (en musique on les cale à la croche ou à la noire)

CMD 4 pannaux de controle de l’écriture des automations.

SUSPEND (arrete lecture et écriture des automations, fonctionne comme un ALT plus Automation OFF)

 

### Paramètres diponibles en automation

Dans la fenetre d’effets : 

j’ai besoin d’un seul paramètre : CTRL CMD Clic (CTRL START ALT Clic) → rend le paramètre éditable

Si j’ai besoin de tous les parametres du plugin : CTRL ALT CMD et on clic sur la double fenetre dans la section AUTO

External layback permet d’eregistrer le mix sur une autre machine

ALT CMD B ou File→Bounce Mix : La fonction bounce disk ou bounce mix

Quand on bounce il faut 

choisir un nom et un format

Choisir une sortie (output bus or internal)

On peut y coupler une version mp3

On choisit le type de fichiers : Interleaved, Multi mono ou sommation mono

Si on export pour de la vidéo : il faut cocher : Pad To frame Boundary

cela l’oblige à commencer le bounce sur une image fixe

On peut importe le bounce dans la session après sa réalisation

Choisir la localisation du bounce 

Offline 

External layback ne permet pas le offline

# CHAPITRE 10 : Export

### Print mix ou bounce to track

prendre les sous groupe et de les envoyer dans un bus internes puis dans une piste. 

pratique pour garder le mix dans la session

ne permet pas le offline

### Backup vs Archivage

Setup→Preference→opération > autobackup

Permet de choisir le nombre et le temps (1 minutes mini) 999 backup max

je sais que je suis sur un backup car l’icone est en blanc au haut de la session. Il ne faut jamais travailler sur ce genre de session. Il faut toujours l’enregistrer avant de travailler dessus. 

Archivage : 

Règle d’archivage des datas en studio : 

La regle des 3-2-1 

tu veux archiver une session : tu dois avoir trois backup dans deux lieux différents. 

Le deux lieux différents est très important ! 

En aucun cas on archive sur des clouds publics! Cloud privé obligation pour de nombreux studio. Sinon mise en défaut pour non protections des données. (boite spécialisées)

il faut savoit ou sont les données quelles sont les clées de cryptages, est ce que le provideur à acces aux données.

Projets dans lesquels la sécurité des data est indipensable (grosses boites)

Pour faire ça on va utiliser la fonction : file→save copy

Permet de sauvegarder dans les différentes versios de protools. 

Il permet de transformer une session en project et un project en session. 

On ne peut pas transformer une template en session ou une session en template.

Ensuite on choisit ce qu’on veut copier dans la session copié (généraement les audio et vidéos files)

Le nom générique c’est copy of …. (cette copy on l’a met dans un dd d’archivage et dans le cloud)

Après un save copy in on reste sur l’ancienne session (différent du save as ou on est sur la nouvelle session)