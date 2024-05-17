---
aliases: 
Matière:
  - Protools
Semestre:
  - B2-2
Date: 2024-04-15
Prof: "[[Alexandre Badagee]]"
Type: notes de cours
tags:
  - cours
  - protools
---
[# Certification Protools - 110
Date: [[2024-04-15]] 


# Chapitre 1 -Sessions options 

##  Play-back engine 
Si protools studio artiste - sans session → protools reste ouvert
Si pas Protools ultimate - dans une session → protools doit se fermer et se reouvrir 
Si protools ultimate avec carte HDx ou native → Protools va dans tout les cas devoir redémarrer 

### Buffer size 
Buffer size de low latency 
Buffer size de high latency est régler en fonction des réglages de la frequency 

Plus le buffer size est petit plus cela demande de la ressource à l'ordi, plus le buffer size est grand moins il demande de ressource à l'ordi. 

Input audio → En input, monitoring ou en rec 
Seule les auxiliaire input qui auront une entrée physiques seront dans le buffer size de low latency. 
Soit les piste intruments avec une entrée physique 

Tout le reste passe dans le buffer size de high latency 

### Video engine 
Pour de la video il faut l'activer. 
Si video engine mais pas de video, cela prend de la ressource quand meme.

### Optimisation 
Cela sert à optimiser sur les setup avec une petite puissance 
#### Error during playback/record 
ON peut demander à outre passer ces erreurs sur le main ou sur les aux I/O 
La ressource que ça va prendre peut être minimiser.  Cela va ajouter au minimum 128 samples, parfois plus interessant d'être à 256 sample de manière fixe plutôt quand cochant la correction d'erreur avec 

#### Dynamic plugin processing 
Protools va adapter la ressource que les plugins prennent par le CPU. Sinon meme si le plug est un instrument est que la piste n'est pas jouée le plug prendra de la resource. 
Donc quand il n'y a pas de clip pas de ressource prise par les plugins. 
Cela sauve environ 30% de capacité supplémentaire. 

#### Low buffer size 
Low buffer size ce sont les deux premiers buffers de la liste. Sur des buffer faible pt va optimiser le buffer size pour éviter les arrêts et les artefacts. 

#### Limite number of real-time threads. 
Limiter la puissance pour toutes les taches qui ne sont pas des taches liées à protools. 
Utile sur des setup border. Si gros problèmes de système. 

#### Intel turbo boost 
Valable que pour les plateformes mac et pas sur les mac avec les puces M 

### Disk playback 
#### Cache size
L'audio est stocké directement sur le SSD, pour que ce soit plus rapide, on peut demander de stocker l'audio dans la RAM 

- Normal : au fur et a mesure de l'utilisation il va aller prendre de la ram → **RAM Dynamique**
- Ou alors on donne une valeur fixe de ram. Que l'on utilise ou utilise pas la ram, il y aura 8Go ou la valeur choisie inutilisable par le système. 
Avid déconseille d'utiliser les deux derniers slots car cela enlève trop de RAM au système. 
La valeur peut être adapter pendant la session. 

## Hardware 
Dans cette fenêtre deux situation : 
Si interface AVID je vais avoir toutes les options pour contrôler la carte depuis protools 
Activer phantom, ou micro etc…. Permet de controller sans toucher physiquement 
Sinon on a juste le launch setup app qui va lancer l'AMS audio midi setup qui va permettre notamment de configurer protools aggregate. 
Qui permet de combiner plusieurs carte sons. 

L'interface affiché est celle du playback engine. 
## System Usage
Menu window > système usage 
Memory donne le pourcentage de ram retirée au système global.  
Disk cache : quantité de RAM utilisé sur la quantité réglée. 

Si on est en dynamic, le disk cache disparaît et le taux de charge du bus donnant accès au SSD 

Au dessus on a l'utilisation du disk par protools. 
Le Total n'est pas une somme de l'ensemble d'utilisation des coeurs. 

Certaine tache ne seront pas mise en cœur 
Automation clip effect clip gain et élastique audio seront des taches calculés par le cpu de l'ordinateur. 

### Session setup

{CMD + num2} → Donne la carte d'identitée de la session. 
On peut modifier le interleaved, l'audio format et le bit depth mais ce n'est pas rétro actif. 

À droite : capacité de choisir les différents sample rate et frame rate en fonction du projet. 

Menu setup I/o > setup 

## I/O setup 
Tout ce qui est input et output reflet le physique du système sur lequel on est 
Le reste c'est le numerique. 
Le bus suit la session. 

On peut supprimer les chemins et les construites. 
On peut utiliser **CMD + N** pour en créer un nouveau. les raccourcis de creations de piste marche ici. On peut demander une assignation auto ou manuel. 
ON peut créer de sub-path, mono et avec l'assignation automatique il va créer les deux subpath en mettant les deux différents canaux pour chaque subpath. 

On peut les activer ou les désactiver. Attention sélectionner ne veut pas dire actif 
Pour les outputs et les input c'est la meme chose. 

Si la carte n'a pas de sorti et que l'on crée plus de chemin que le nombre de sorties. Il est alors unavailable. Écriture italique 
Le chemin avec le monitor. Est la sortie de monitoring. 
Si on change le monitor et les output il faut les patcher dans les bus pour que cela reste 

Audition path est le chemin qui permet la lecture en preview. Toutes les écoute ou on utilise pas la barre d'espace. Ce trouve en bas à droite de la fenêtre I/O 
Le terme play et preview est en bas de la fenêtre pt. 

On peut renommer depuis cette fenêtre ou depuis la session. 
On peut créer un path avec directement les subpath. En cas d'oubli on peut utiliser la creation de subpath par défaut.

En cliquant sur **default** on retrouve la config par défaut. 
Mais si il y avait des bus renommés et utiliser il va les garder. 

Output bus est un bus relié à une sortie physique. 
Internal bus est un bus qui n'est pas relié à une sortie physique. 

Toutes les sorties sont **des bus**, internal ou output. 
Dans la session : 
- Quand le path in available→ path n/a 
- Quand path inactif → path inactive

En cliquant sut format dans I/O setup on peut changer le type de bus (de mono a stereo ou plus) par contre cela ne crée pas les subpath. On peut changer que les bus inutilisés. 

Ce qui apparait dans la session l'ordre est le meme que l'ordre dans la liste d'I/O Setup. Donc on peut le reorganiser les bus dans I/O Setup. 

On exporter les settings du I/O setup si on veut l'utiliser pour d'autres session. 
Créer un fichier .PIO dans document>protools. Dans la fenêtre de dashboard on va retrouver le I/O setup que l'on aura exporter. 

Quand on importe, cela importera que la table sur laquelle on est. Pour importer l'intégralité il va falloir cliquer sur **ALT + click** ou il faut cocher apply to all tables pour appliquer sur l'ensemble des tables. 
On peut utiliser un .pio ou un .ptx comme fichier d'import. 

Restore : Il faut d'abord cliquer sur show last saved setup puis ensuite on valide avec restore from session. Il fonctionne comme l'importe. Il faut soit ATL + click ou cocher la case apply…
Valider le quizz = 8/10 
# Leçon 2 : Organisation dans la session 

## Module de zoom 
Les zoom verticaux sont indépendants. 
On a 5 presets enregistrables. **CMD + CLICK** cela permet d'enregistrer le zoom. 
On peut les appeler avec les touches numéro de l'alpha numerique (chiffres au dessus des lettres.) 
Vérifier que dans setup > editing > Touche de 1-5 soient associées au zoom preset. 

F5 : outil de zoom avec alt cela permet le de zoom 
Si on rappuie sur F5 on est en single zoom cela permet de zoomer et il va ensuite remettre l'outil precedent. Il va rebasculer sur l'outil d'édition précédemment utilisé. 

Touches pour zoom : **R T** 

### Zoom toggle 
E si raccourcis rapides activer sinon icon avant l'outil zoom. 
Preference > Editing > 
Permet de définir la taille d'une piste quand on click sur le zoom toggle 
Qu'elle vu va apparaître par exemple en waveform. Ou no change. 
Le zoom toggle s'applique sur toutes les pistes ou il y a le sélecteur. 

Zoom toggle follow edit → Le zoom reste actif et sera appliqué sur la piste sélectionnée 

Autre option avec moins d'utilité. 

Suivre édite selection est vraiment pratique. 

### Selections 
Si je veux me placer à un endroit précis : asterix du pavé numerique. On a juste a rentrer la valeur 
/ slash Du pavé numerique permet de faire une sélection 
"* "  donne un point précis.

Les flèches rouges ne signifient pas enregistrement. Quand les flèches sont rouges, cela veut dire qu'il y a une piste armée en enregistrement. 

En prenant les flèches bleues ou rouges on peut changer la taille de la selection en les drag
Avec **ALT + drag** on peut déplacer la selection sans changer sa longueur.

Sur des grosses sessions. 
## Navigation 
### Univers 
ALT + num7 active le universe 
On peut l'afficher via le menu de la toolbar, la flèche ou le menu view. 
On peut décaler le carré blanc pour se déplacer rapidement. On peut aussi simplement cliquer sur le univers. 
Les pistes auxiliaire, VCA Master fader va les symboliser avec du blanc. Il symbolise que les pistes avec du son. En couleur. 
### Memory location 
On a 32000 memory location max par session. 
**CMD + num5** ouvre la fenêtre des memory location. 

On peut les créer en marker pour se repérer dans notre session. 
**Pour ajouter un marker** : Enter du numpad ou le plus de la marker ruler. Soit dans menu>window> memory location 

On choisit si le marker est en bar beat : relatif = flèche 
ou en absolue : time = losange

Récemment on a des markers dans la ruler mais on a aussi des marker de pistes 
**CMD + Enter numpad** → le marker sera associé à la piste. 

On peut choisir les options que l'on veut garder quand on selection ce marker. 

Pour recall un marker : 
Cliquer dessus. 
Cliquer sur la memory location dans la memory location 
 Faire avec le clavier .le chiffre. 

On peut aussi faire des selections **.3. SHIFT .4.**
Le point (virgule sur Azerty) du numpad 
 On peut aussi faire click shift click sur les deux marker 
Si je fais enter du pavé numerique puis on va sélectionner selection et les options que l'on veut 

Pas besoin de garder la selection 

Il y a donc des memory location en selection pour rappeler des zones spécifiques 

Pratiques pour mettre les différentes séquences ou les morceaux d'une musique 

Memory location none 

Permet de memoriser des affichages.  Permet de rappeler des visualisation différentes des pistes. 

**CMD + Clic** sur le ruler ouvre l'édit du  marker. 

On peut édite dans la fenêtre memory location 
Clic droit edit memory location. 
Avec la touche CTRL + click sur la memory location  ouvre la fenêtre d'edit
SI on double click sur la memory location ouvre la fenêtre d'edit

Pour supprimer 
Alt click 
Ou click droit, remove 

Dans le menu on peut tout delete si besoin via le menu de la fenêtre. 

### Window configuration 
new Window configuration 
**CMD + Shift + J**  pour afficher la fenêtre 
ou menu window>conf>New window configuration 

Pour afficher la window 

. + "le chiffre + Astérix pour rappeler la config. 

.+ ouvre la fenêtre new windows config directement 
Point + "+" → Créer une nouvelle window configuration. 
Le point du numpad 
Attention c'est la virgule sur le numpad azerty. 


On peut les licker a des memory. 

Dans le menu d'edit memory on peut recall aussi les window configuration. 

# Folder tracks 

2 types basiques ou routing 

Pas de format pour le basique 
Format à choisir pour les routing. 
Il y a des choses communes pour les deux : 
Solo, mute, indicatif audio 
Capacité de les mettre dans des groupes de pistes. 

Routing folder tracks : 
Il y a les inserts, les sends, accès au niveau et panoramique. Il remplace les aux input. 
Les routings servent donc de sous-groupe ou sous-groupe intermédiaire. 

Quand on crée des piste qd il y a déjà des routings folder tracks. 
S'il est sélectionné il va mettre la piste directement dans le folder track. 
Sinon il va créer une piste normalement. 

Quand on supprime un dossier on peut tout supprimer ou juste le rangement et garder les pistes qu'il contient. 

Les pistes dans un folder non pas obligatoirement la couleur du folder. 

Codes couleur réglés dans setup > preference > display. 

### Couleur 
Couleur de bases
Track and midi devices channel  toutes les pistes midi  qui auront le meme. Channel seront de la meme couleur. 
Toutes les pistes qui on les meme device 

Pour changer la d'une piste : menu Window > Color palette. 
Avec la color palette ou peut choisir en haut à gauche le type de ce qu'on veut changer. 
HOLD permet de garder la couleur quand on sélectionne une piste. 

Ne cliquant sur default, la couleur sera celle du setup preference et default track color coding. 

Lorsqu'on a des routing folder tracks 
Si je veux mettre une piste dans un folder : 
- Drag and drop o 
- sélectionner la piste → move to 
- **Shift + Alt + CMD + N** → move to new folder les pistes sélectionnées, on peut demander que la sortie de routing soit automatiquement mappé sur le bus du folder track. 
On peut le faire depuis la track list. 

Folder track 
**SHIFT + F** cela ouvre le folder attention cela permet d'ouvrir un basique ou routing folder track si le curseur est sur le Folder track. (Possible d'en ouvrir plusieurs)

>[!note] 
>**CMD + double clique** → créer piste audio 
**Shift + Double Clic** → master fader 
**Alt  + Double Clic** → instrument 
**CTRL + Double Clic** → AUX
On peut les combiner pour créer plusieurs pistes 

Du dernier format crée sauf pour la piste instrument qui sera forcément stereo 

### Batchrename 

Click droit batch rename 
OU **shift + alt + R**  une fois que les pistes sont sélectionnées 

Il y a quatre categories. 
- remplacer 
- Trim (enlever des caractères par devant ou par derrière)
- Ajouter 
- Numéroter 

Il y a 5 presets que l'on peut enregistre avec **CMD + CLIC** pour enregistrer le preset 
Il est possible de faire des save settings as si on en veut plus.

### Navigation 

Shift + S → Solo
Shift + M → mute (? En azerty)
Shift + I 
Shift + R 
Concerne les pistes sélectionnées avec le curseur 
**Shift + T**  = links track and curseur linked 
Menu dans tracks 

### Solo et Mute 

Dans le transporteur le s indique s'il y a un solo ou en mute 
En cliquant su le s on peut desoloiser toutes les pistes mais pas avec le M 

### Recherche pour naviguer 
Scroll to track 
ALT + CMD + F ou menu track scroll to track 
Cela place la piste en haut de l'écran sans changer son ordre. 
Si la piste est dans un folder fermé il va ouvrir le folder track et mettra la piste en haut. 

Scol to track haha 
#### Scroll into view 
**SHIFT + CTRL + CLIC** sur la piste et la piste arrive en haut 
Ou clic droit scroll into view 
Cela place la piste en haut de l'écran. 
### Rendre pistes inactives 
Clic droit make inactive ou **CTRL + CMD + CLIC** sur l'icône de la piste uniquement sur la fenêtre de mixeur. 
Si la piste est mise dans un folder actif la piste restera inactif 
Si le folder est inactif, toutes les pistes qui sont a l'intérieur sont inactives. 
Si la piste est actif dans un folder inactif en la sortant du folder elle redevient inactive 

### Bases des pistes 
Audio, aux, vca, master, routing folder → sont de bases en sample base

Midi et instrument → sont en tick base\

# Chap 4 : clip list 

Les raccourcis de base c'est SHIFT + CMD
### Batchrename 
**SHIFT + CTRL + R**, qu'on peut trouver dans le menu de la clip list 
Car avec CMD c'est renommer **shift + CMD + R** = renommer

On peut choisir en fonction de l'ordre de la timeline ou l'ordre de la clip liste

ALT + CLICK permet de faire une preview dans la clip list 
Attention il faut un audition path pour que ça marche.

Il y a les meme options de couleur sur les clips. 
On peut avoir une coloration des clip en fonction des markers. 

Si on change la couleur d'un clip unique, il ne sera plus affecté par la couleur par défaut. 
Il est possible de mettre les couleurs dans la clip list aussi. 
Pour afficher la couleur choisie dans la clip list il faut l'activer dans les paramètres. 

### Groupes de clip 
**ALT + CMD + G** ou clic droit > Groupe ou menu clip list groupe. 
On peut les faire avec des clip audio, MIDI, video et mixtes. Avec tous les types de media. 
On peut faire des groupes avec de pistes si la sélection est continue. On peut pas faire 1 et 3 on peut faire 1,2,3. 

On peut faire des groupes sur des pistes qui sont continues et discontinue. (De haut en bas)

Le groupe de clip est selection based 
L'icône en bas du clip donne l'info de ce quelle contient. 
La ligne brisée indique que les différentes pistes du groupe ne sont pas à coté
Carré = groupe mixte 

Dans la clip liste on peut avoir plus en detail la contenance du groupe. 

Pour dégrouper : **ALT + CMD + U** ou clic droit un groupe 

SI j'ai besoin de refaire le groupe on peut regroupe avec **ALT + CMD + R** ou clic droit regroupe 

Pour le regroupe on a pas accès dans le menu clip. 

On peut dupliquer un groupe 
SI on modifier un groupe qu'on a déjà dupliquer soit on copie et crée une nouvelle entité ou on applique la modification à tous les groupes qui avait le meme nom 

Si on utilise souvent des whoosh ou autre on peut exporter les groupes. Attention on exporte le groupe mais pas l'audio. Donc le faire plutôt avec des clips qui appartiennent a une banque de son et pas par rapport à une session. 

### CLip looping 

**ALT + CMD + L** 
Ou click droit loop
On ne peut pas looper deux clip qui se trouvent sur la meme piste. Possible de looper des clip different sur des pistes différentes mais un seul clip par piste. 

Trois options 
- nombres de boucle 
- Longueur en mesure
- On boucler jusqu'au prochain clip on jusqu'à la fin de la session. 
On peut ajouter des fades. 

On peut changer la longueur de la boucle tout en gardant la longueur de la boucle. 
Si le sélecteur est sur la flèche de loop on va sélectionner que des boucles sinon si on est sur la partie supérieure on sélectionne normalement. 
Pour découper → Menu>clip> unloop ou clip droit unloop 
Deux choix : 
- remove revient à la boucle d'origine
- Flatten : va afficher les boucle de manière individuelle 

Un groupe de clip peut être boucler. 

Pour loupe deux clip sur une meme piste il suffit de les grouper. 

# Playlists 

Quand on crée un piste on est sur la playliste 0 

Quand la pist**
**CTRL + \ (backslash)** (livre sterling sur azerty) 

Quand flèche bleue c'est qu'il y a au moins deux takes 

Permet de faire des takes sur une meme zone sans polluer son écran. 

CTRL + CMD + backslash  
Permet de dupliquer la playlist que l'on vient de créer. 

Pour avoir des bases de différentes il faut de sélectionner la playlist. 

Delete unused playlists : Une playliste affiché est une playliste utilisé. Si tu n'es plus en vue playlist il va proposer de les effacer. 
Il faut donc que les playlistes soient inutilisées donc vides ou qu'on ne les voit pas. 

