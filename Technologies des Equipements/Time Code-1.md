---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-11
Prof: David Laurent
Type: notes de cours
---
# Time Code-1
Dates: [[2023-10-11]] | Tags : #cours #Technologie-des-équipements

#### Objectif
Étude du système de repérage absolu des images en heures, minutes, secondes et nombre d'images, normalisé au niveau mondial. Notions de synchronisation et modes d'utilisation en particulier dans le cas du son à l'image. 
## Introduction
#### 1. Definitions
- **synchronisation** : Action de rendre solidaires et simultanés les mouvements de deux appareils
- **synchrone** : Se dit des mouvements qui se font dans un même temps (son synchrone c'est les sons enregistrés sur le plateau, on l'appel aussi son 

> [!NOTE]
> Il faut environ 3 images (120ms) de décalage entre image et son pour pouvoir établir précisément le sens du dé-synchronisme. EN revanche un décalage d'une seule image est détectable par un œil et une oreille exercés. À une image c'est dur de dire si le son est en avance ou en retard

- Historiquement c'est le support Image/vidéo qui "porte" le Time Code (Master), et le ou les supports (ou appareils) du Son qui seront asservies (Slave). C'est l'image qui porte la synchronisation. (Il est possible de le changer, c'est une norme historique)
- La CST (Commission Supérieure des Techniques de l'image et du son) indique les limites de perception et limites maximales admissibles de la désynchronisation Son/Image en diffusion pour la télé : -1 ou + 2 images max.
- Il existe des générateurs de timecode, dans ces cas là, ni la vidéo ni le son ne son maîtres, ils sont tous les deux slaves.  
## Les Codes SMPTE/EBU
### 1. Origine 
Le TIme Code est né du besoin de caractériser chaque image dans le domaine de la vidéo pour faciliter le montage. Ce système de repérage absolu a donné lieu au tout début des années 70 à 2 variantes normalisées Au départ en fonction du nombre d'images par secondes: 
- Le SMPTE (Society of Motion Picture and Television Engineer) pour les systèmes 30i/s
- L'UER (EBU en anglais) (Union Européenne de Radiodiffusion) pour les systèmes à 25i/s
Rappel : le format initial au cinéma (sur pellicule) est de 24i/s

> [!NOTE]
> Il existe des variantes concernant le nombre d'i/s par exemple le 29,97 qui correspond au système vidéo couleur américain NTSC (petite blague accronyme = Never Twice the Same Color)

 Représentation du Time Code : **HEURE : MINUTES : SECONDES : N° D'IMAGES**
 Exemple : 02:36:23:04
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

|  Heures     | Minutes    | Secondes   | N° Images |
 | ---------- | ---------- | ---------- | ---------- |
 | Diz./unit. | Diz./unit. | Diz./unit. | Diz./unit. |  
 | (2 + 4)    | (3 + 4)    | (4 + 5)    | (1 + 8)    |    
 | 24         | 34         | 45         | 18         |    

Il faut également intégrer un mot de synchro pour le début et la fin de chaque information composé de 26 bits
