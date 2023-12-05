---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-11
Prof: "[[David Laurent]]"
Type: notes de cours
---
# Time Code
Dates: [[2023-10-11|2023-10-11]] - [[2023-10-12 1|2023-10-12 1]]  | Tags : #cours #Technologie-des-équipements

>[!INFO] Objectif
>Étude du système de repérage absolu des images en heures, minutes, secondes et nombre d'images, normalisé au niveau mondial. Notions de synchronisation et modes d'utilisation en particulier dans le cas du son à l'image. 
## Introduction
#### 1. Definitions
- **synchronisation** : Action de rendre solidaires et simultanés les mouvements de deux appareils
- **synchrone** : Se dit des mouvements qui se font dans un même temps (son synchrone c'est les sons enregistrés sur le plateau, on l'appel aussi son 
- 
> [!NOTE] Notabene 
Il faut environ 3 images (120ms) de décalage entre image et son pour pouvoir établir précisément le sens du dé-synchronisme. EN revanche un décalage d'une seule image est détectable par un œil et une oreille exercés. À une image c'est dur de dire si le son est en avance ou en retard

- Historiquement c'est le support Image/vidéo qui "porte" le Time Code (Master), et le ou les supports (ou appareils) du Son qui seront asservies (Slave). C'est l'image qui porte la synchronisation. (Il est possible de le changer, c'est une norme historique)
- La CST (Commission Supérieure des Techniques de l'image et du son) indique les limites de perception et limites maximales admissibles de la désynchronisation Son/Image en diffusion pour la télé : -1 ou + 2 images max.
- Il existe des générateurs de timecode, dans ces cas là, ni la vidéo ni le son ne son maîtres, ils sont tous les deux slaves.  
## Les Codes SMPTE/EBU
### 1. Origine 
Le TIme Code est né du besoin de caractériser chaque image dans le domaine de la vidéo pour faciliter le montage. Ce système de repérage absolu a donné lieu au tout début des années 70 à 2 variantes normalisées Au départ en fonction du nombre d'images par secondes: 
- Le SMPTE (Society of Motion Picture and Television Engineer) pour les systèmes 30i/s
- L'UER (EBU en anglais) (Union Européenne de Radiodiffusion) pour les systèmes à 25i/s
Rappel : le format initial au cinéma (sur pellicule) est de 24i/s

> [!note] Notabene
> Il existe des variantes concernant le nombre d'i/s par exemple le 29,97 qui correspond au système vidéo couleur américain NTSC (petite blague accronyme = Never Twice the Same Color)

 Représentation du Time Code : **HEURE : MINUTES : SECONDES : N° D'IMAGES**
 Exemple : 
> 02:36:23:04
 
 *Europe Première image = 0; dernière 24
 États-Unis : Première image = 0; dernière 29*
 
Le Time Code est apparu avec l'évolution des montages vidéos et la nécéssité de pouvoir gérer la synchronisation. 

Quand on est sur protools c'est pour ça qu'on adapte le time code du son au time code de l'image

Le Time Code comprend différents types d'informations : 
- Les données temporelles : représentant l'adresse de chaque image en Heure, Minute, Seconde, Numéro d'IMAGES 
- Les données utilisateur (User Bits) : Permettant à l'utilisateur d'inscrire ses propres informations de repérage des supports (Cassettes Vidéo à l'époque)
- La synchronisation : information nécessaire pour délimiter les informations du code.
### 2. Constitution binaire du codes 
Il s'agit d'un signal déci-binaire (DCB= Décimal Code Binaire) qui permet les chiffres de 0 à 9 en une suite nombres binaires
L'idée est de coder séparément les chiffres des unités et des dizaines de chaque élément du TC 
Codage binaire des chiffres de 0 à 9 :
Ainsi selon le type de donnée à coder, il faudra un mot binaire plus ou moins grand : 

| Chiffre décimal à coder | Représentation Binaire | Chiffre décimal à coder | Représentation Binaire |
| ----------------------- | ---------------------- | ----------------------- | ---------------------- |
| 0                       | 0000                   | 5                       | 0101                   |
| 1                       | 0001                   | 6                       | 0110                   |
| 2                       | 0010                   | 7                       | 0111                   |
| 3                       | 0011                   | 8                       | 1000                   |
| 4                       | 0100                   | 9                       | 1001                   |

- 2 bits pour dizaines d'h ou images (car de 0 à 2 en décimal)
- 3 bits pour dizaines de min ou secondes (car de 0 à 5 en décimal)
- 4 bits pour toutes les unités H,min,sec, im (car de 0 à 9 en décimal)
Ils ont cherché à alléger le plus possible en séparant les unités et les dizaines pour simplifier le code binaire du Time Code. 

| Heures     | Minutes    | Secondes   | N° Images  |           |
| ---------- | ---------- | ---------- | ---------- | --------- |
| Diz./unit. | Diz./unit. | Diz./unit. | Diz./unit. |           |
| (2 + 4)    | (3 + 4)    | (3 + 4)    | (2 + 4)    | = 26 bits | 

Il faut également intégrer un mot de synchro pour le début et la fin de chaque information composé des 26 bits de chaque image. Ce mot appelé **Sync Word** est composé de sorte à pouvoir être identifié facilement : 00 111111111111 01 = 16 bits. La suite de 1 n'existe pas en codage horaire et les extrémités 00 et 01 indiqueront le sens du défilement au système de lecture du TC. 
Cela permet donc de lire le time code dans les deux sens du défilement, en lecture ou en retour rapide arrière. 
Il faut donc au minimum 26 + 16 = 42 bits. Il a été choisi d'attribuer **80 bits** pour chaque image afin d'intégrer les User Bits (Groupe Binaire d'utilisateur)

- [1] Débit en 25 I/s : 25x80 = 2 kbit/s
### 3. Représentation électrique
Initialement le Time Code a été conçu pour être enregistré également sur une bande magnétique audio, il faut que sa représentation électrique soit compatible avec les enregistreurs analogiques dont la bande passante en fréquence est limitée. 

La représentation initiale est le NRZ (No Return to Zero), elle est peu compatible car une suite continue de 1 ou de 0 n'est pas conseillée pour les circuits audio. On a donc choisi la représentation **Bi-Phase Mark** (Manchester dans le cours sur l'audio numérique) pour le Time Code :
- Changement de niveau (haut-bas / bas-haut) à chaque changement de bit, maintien de la valeur durant un bit 0 et changement à la moitié d'un bit 1. Cela permet au signal d'être auto-synchronisé. 
- Le résultat est un signal carré dont la fréquence oscille entre 1 et 2 Hz
Donc il est audible, on peut donc l'enregistrer et le manipuler avec les appareils audio.

[Exemple de Son du Time Code](https://youtu.be/zjH0RFV206M?si=6gzyBxuyRZvv3WG5) 

*Les codages NRZ et Biphasé Mark*
Explication de la différence entre ce signaux ici : [[Codages des signaux]] 

## Les différentes Formes
### 1 Le LTC (Longitudinal ou Linear Time Code)
On appelle LTC le Time Code enregistré sur une piste longitudinale séparée de l'image. Le TC est écrit le long de la bande. C'est une tête fixe qui lit le LTC.
*Il est transporté soit :* 
- avec un câble coaxial + BNC
- avec un câble symétrique + XLR
*Avantages :* 
- Débit faible
- Transport, distribution, amplification possible par les équipements audio analogiques
- Lecture possible à grande vitesse de défilement (recherche rapide)
- Lecture dans les 2 sens avant et arrière.
*Inconvénients :*
- Pas de lecture possible en stop car la bande a besoin de défiler pour que le code soit lu. 
- Lecture difficile au ralenti
### Le VITC (Vertical Interval Time Code)
On appelle le VITC le Time Code incorporé à l'information image vidéo analogique. Il se compose de 90 bits inscrits 2 fois par trame : 26 bits d'informations temporelles + 9 x 2 bits de Synchro + 8 bits de correction d'erreur + 32 User Bits. La représentation électrique NRZ est adaptée ici car les équipements vidéo sont plus performants que les enregistreurs pour le Son. (Le changement c'est pour s'adapter aux technologie d'écriture de l'image sur la bande)
Débit en 25i/s : (90 x 2) x (25 x 2) = 9kbits/s

C'est un tambour et non plus un tête fixe. Du coup le time code est inséré dans le code de la vidéo. Quand on fait pause le tambour continue de lire le code même si la bande est en pause ou au ralenti. 

Avantages : 
- Lecture possible à l'arrêt sur l'image.
Inconvénients :
- Illisible en vitesse rapide.

### 3 Le ATC (Ancillary Time Code)
On appelle ATC le Time Code incorporé dans la partie horizontale (HANC horizontal Ancillary) des données de l'image vidéo numérique. Il peut contenir le LTC et/ou le VITC.
Il existe deux formats :
- ATC norme SMPTE i88 R : Vidéo 8 bits et 10 bits (avec 16 HANC data words)
- ATC norme SMPTE RP 196 : Vidéo 10 bits (avec 10 HANC data words)

> [!NOTE]
> On parle de D-VITC (Digital VITC) en vidéo numérique SD.

### 4 Le serial Time Code
On appelle Serial Time Code le TC incorporé en série au protocole de télécommande RS 422. Le RS 422 est un protocole série asynchrone permettant le transfert de données aller/retour avec un débit de 100 kbits/s à 1 Mbit/s sur une longue distance(signal symétrique). Les infos principales qu'il véhicule sont le transport (play, stop, rec…), le track arming, le choix du mode du magnétoscope vidéo (assemble ou insert), le TC….
Le connecteur habituel est le SUB-D9 pins mais il existe des adaptateurs USB. 

C'est un time code pour échanger entre les machines, c'est une méthode de transport. les time code précédent servaient plus à l'enregistrer sur les supports.

> [!NOTE]
> Le protocole RS 232 est identique mais en liaison asymétrique.

### 5 Le MTC (Midi Time Code)
On appelle MTC le Time Code incorporé au protocole MIDI(Musical Instrument Digital Interface) utilisé pour la communication entre instruments électroniques, contrôleurs, séquenceurs, et logiciels de musiques. Il permet la synchronisation de ces différents équipements.

### 6 Notions complémentaires
#### Offset
On appelle **Offset** un décalage volontaire ou involontaire du défilement d'une machine par rapport aux autres. Lorsque l'on applique un offset positif ou négatif, les machines concernées continuent de défiler à la même cadence mais avec un décalage. 
C'est utile pour le montage pour s'adapter au TC reçus qui parfois on un offset. 

C'est un décalage volontaire dont on demande à la machine de tenir compte et de façon fixe. 

#### Jam sync 
Mode de synchronisation  que l'on peut activer sur une machine définie en mode slave dans une chaîne d'appareils synchronisés. Cela permet à cette machine de continuer à défiler un certain temps sur la même cadence lorsque le TC envoyé par la machine Master est interrompu ou illisible.
Dans un mode standard dès que la machine ne reçoit plus de TC ou un TC défectueux, elle se STOP.
Utile sur des prises longues ou des prises ou le ne veut pas de coupure en cas de problèmes.
#### Free Run 
Mode de synchronisation qui consiste à utiliser le Time Code interne d'un appareil qui défilera de manière continu et sans interruption. L'utilisateur peut choisir un TC de départ ou alors l'appareil se synchronisera temporairement sur un TC externe le temps de se caler sur cette horloge. 
Ce mode est fréquemment utilisé lors des tournages en multi-caméra + enregistrement sonore afin d'assurer que tous les appareils enregistreront leurs médias (image et son) avec le même TC ce qui facilitera le travail de post production. Dans ce mode, le TC continue de tourner même si l'appareil est en stop. 
#### Rec Return 
Mode de synchronisation dans lequel le TC ne défile que lorsque l'appareil est en enregistrement. Si on stoppe la machine, le TC s'arrête et reprendra depuis cette valeur au prochain lancement de l'enregistrement. 
#### Générateurs de TC`
Il existe des générateurs (portables ou non) de Time Code souvent en BNC et aussi HF (sans-fil)
Examples de générateurs : *Horita PTG2 - Atomos - Ambient*

>[!NOTE]
> Les fichiers audio .BWF (Broadcast Wave File) incorporent le time code dans les Métadatas (c'est la différence avec le Wav qui ne l'incorpore pas)