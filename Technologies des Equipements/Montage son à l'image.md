---
Matière:
  - Pratique
  - Technologie des Equipements
Semestre:
  - B2-1
Date: 2023-12-11
Prof: "[[Jean-Lionel Etcheverry]]"
Type: notes de cours
tags:
  - cours
  - pratique
  - Technologie-des-équipements
---
# Montage son à l'image
Date: [[2023-12-11]] 

Le Rec de la voix c'est le nerf de la guerre.
Voir à quelle point la prise de son négligente à un impact sur la compression du dialogue. 

Avant on va d'abord faire un montage sonore ou il est possible de pré-mixer quand même. Puis on mix (une après midi).
Une partie des voix est off, donc il faudra la rec. `

Dans un milieu broadcast, on va utiliser trois outils principalement (AVID Média Composer, DA VINCI Resolve, ADOBE Premiere), une fois que les monteurs on fait leur taffs, il va y avoir un montage son et un montage images, qui va résulter en un master une fois que l'ingé son l'a mixé. 
Du montage images les monteurs vont sortir un fichier vidéo témoin, et ils vont envoyer une session audio. (Il ne faut pas mixer un montage son qui sort d'un montage image) donc il faut apporter du son et densifier le projet. 
On utilise donc, Nuendo, Pro-Tools ou Audition. (Apparemment, Nuendo est une tuerie). 
Même si monopole de Pro-Tools. 
Le monteur image, doit passer par un export AAF EMBEDDED (montage des clips audio, noms, markers, niveaux, fondus, etc) que l'on va pouvoir ouvrir dans le logiciel de notre choix. 
**C'est un point de départ** (part contre on ne peut pas double cliquer sur un AAF) car c'est souvent un mauvais point de départ, il est plus intéressant de crée une session protools ou on importe ensuite le AAF (comme ça on contrôle la création de la session). 
De la session, on ne fait que sortir un master en WAV 24/48. (Pour le Broadcast). Qui sera utilisé par les monteurs pour sortir le fichier video final. 

Les monteurs n'ont accès qu'a des pas de 40ms (1/25 secondes). Ce qui peut amener des problèmes de phase. 

## Avant le programme
Le temps d'amorce sert à fournir les références technologie-des-équipements (nom du monteur plus tel, plus version)

**DÉCOMPTE** Avant programme : 10 secondes.
**BIP DE SYNCHRO**:
- Image blanche = durée 40ms, soit une image à 25i/s
- Bip de 1000Hz (ce qu'on veut) = durée de 40 ms
Il faut que les deux durent le même temps. 
**START PROGRAM** 2 secondes après le BIP, soit 50images à 25i/s

Cela implique que le son est synchro à l'image : donc tout ce qui est derrière est synchro. 

- L'annonce doit être fixe sur fond noir et visible dès la première image. Elle doit rester à l'écran au moins 2 secondes. 
- Le décompte dure 1 image toutes les secondes. Le chiffre doit être gros et centré, blanc sur fond noir.
- Le chiffre 2 est remplacé par le nombre 1000 (ou une croix ou un image blanche, C'est le repère de synchro son nommé Bipsync. 

## Lancement de session 
Toujours configurer son protools quand on le lance 
Penser au timecode.  Le 24/48 
Déplacments d'images [[Protools]]. 
, → 5 images 
! ← 5 images
Importer : **SHIFT+ALT+i**
On peut bosser sur un programme à pleins de techniciens différents et ensuite on rassemble tout le monde. 
On laisse toute les cases cochés pour l'importation. On peut choisir ce qu'on importe. 

On aime bien mettre le début de session sur un chiffre blanc. 

La perche sera toujours en retard. On se base sur la perche, car la perche est souvent à la distance de la caméra et c'est aussi pour ne pas rentrer dans la zone de proximité des spectateurs. 
La perche sera donc artistiquement plus proche de la réalité. Donc on base le timing du micro cravate sur celui de la perche. → **La perche fait foi !** 

Je prépare des niveaux cohérents (sans compresseurs) 
Des electrons qui s'excitent sur un préamplificateur va ajouter du souffle. Donc on veut les stabiliser pour qu'ils utilisent un maximum de la puissance du préamplificateur. 
On va utiliser les vu-mètres RMS
On peut utiliser le DORRO METER de wave. (Sur le master)
Apparition d'un Timbre c'est 50ms. 

Référence pour une valeur moyen : 0VU, -18dBFS, -4dBu
C'est possible d'aller chercher un -8dbFS -12dBFS pour que notre préamplificateur travaille au mieux. 

### Ensuite on importe la vidéo 
On la synchronise, avec notamment le bip ou le timecode affiché sur l'image. 
Shutter encoder
Shift curl → clip gain 
Molette (dans les pref édition incrément,nt de clip gain) - ( pour afficher les courbes)
Assurer fluidité de la convesation



