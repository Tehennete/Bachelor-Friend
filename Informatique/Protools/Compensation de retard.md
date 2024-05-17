---
aliases: 
Matière:
  - Protools
Semestre:
  - B2-2
Date: 2024-05-07
Prof: "[[Olivier Stalla]]"
Type: notes de cours
tags:
  - cours
  - protools
---
# Compensation de retard
Date: [[2024-05-07]] 

On l'active dans option > mix > affichage 
La compensation c'est protools qui fait la compensation. 
PT peut gérer des retards de ≤  16383 samples ($2^{14}$) 


| RTD  | Retard que génère la piste        |
| ---- | --------------------------------- |
| +/-  | Delay manuel                      |
| Comp | Compensation du retard des pistes |


La piste avec le retard le plus long sera affichée en Orange
Si le mot delay est noté en rouge = Non géré 
Noté en vert = Géré 
Plug : Time adjuster (4 à 8195 samples) c'était la méthode avant la compensation Automatique de latence 

Dans option quand elle est désactiver elle se grise sur la fenêtre de mix 

## Maintenance Protools 
Choix de pilote au boot si on maintien N pt va ouvrir le dialogue de choix de pilote 

"L" permet d'activer : la tête de lecture suit le lecteur. 
- Mode sans échec = désactive tous les plugs au lancement → "SHIFT"
- Messages H/W Buffer Size → Il suffit d'augmenter le buffer 
- Pt refuse de s'ouvrir → Le fichier préférences corrompues = il suffit de le supprimer
Aller dans la bibliothèque utilisateur sur mac : aller > OPT > Biblio 
On va dans pref > com.avid.protools.plist  Et on le supprime (Plist pour preference liste)
App data sous Windows 

Protools devient lent 
- Session située sur un volume externe ou sur le serveur 
- HD Fragmenté 
- Un processeur Occupé (Quitter les apps inutiles)
- Trop de plugins → Freeze ou rendre partiel ou total  
- 
