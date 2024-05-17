---
aliases: 
Matière:
  - Physique
Semestre:
  - B2-2
Date: 2024-05-06
Prof: Jean Claude Rakotoniaina
Type: notes de cours
tags:
  - cours
  - physique
---
# Transmission Numérique
Date: [[2024-05-06]] 

## Generalités
### Canal de communication
Un canal de communication donne une possibilité de communiquer à grandes distances. Ce module représente les signaux extérieurs et le bruit qui affectent la transmission. Évidemment, chaque système de communication a un modèle de canal approprié. L'objectif principal de ce cours est de comprendre les techniques du traitement du signal permettant de communiquer sous différents types de canaux.

La propagation des signaux dans les canaux de transmission peut se faire de selon deux types : 
- **Propagation guidée** : la propagation guidée nécessite u nguide d'onde qui contraint l'onde à se propager selon un certain chemin (Filaire, DD, SSD, K7 etc…)
- **Propagation libre** : La propagation est libre lorsque les informations sont transmises sans dispositif de guidage. (D'où l'accès à l'information dans des wines isolée. Wifi, ondes, Satellite, ondes hertziennes, etc….)
Le canal peut être une ligne téléphonique, une liaison radio, un support magnétique…. 

### Taux Erreur Bits  Ou B.E.R 
Bit error rate en anglais 

TEB = Nombre de bit erronés / Nombres de bits transmis 

$$TEB = \frac{N_{b de bits errones}}{N_{b de bits transmis}}$$
Mepi3 

## Transmetteur numérique 
### Le codage source 
Le codage source compresse le signal numérique en exploitant ses redondances. Pour les contenus multimedias, la compression est réalisée par un CODEC. Elle peut être destructive ou non destructive. Les principaux codecs sont rappelés dans un tableau du polycopié
### Le codage canal 
Ajoute des bits supplémentaires pour détecter et corriger les erreurs dues aux imperfections du canal de transmission. Ce codage augmente le debit binaire. 

Exemple en 4g/5g le code s'appelle le turbo-code

### Codage voie 
Transforme le signal numérique en un signal analogique adapté au canal de transmission.

>[!note] Selon la bande passante du canal, on a le choix entre la transmission en bande de base(canal de type passe-bas) ou sur fréquence porteuse (canal type passe-bande)

## Récepteur numérique 
Elle fera le meme processus mais dans l'autre sens. 

## Transmission en bande de base
Codage en line
### Definition
Quand le signal est émis sans transposition de fréquences, on dit que la transmission s'effectue en bande de base. Le codage électrique

Quand le signal est émis sans transpoistion de fréquence. 

La transmission en bande de base est un codage de voie qui s'effectue en deux étapes : 
- 1ere étapes : le codage des bits en symbole
- 2ème étapes : l'attribution d'un signal analogique q chaque symbole 
On obtient alors un signal physique analogique s(t) correspondant au signal numérique

#### Codeur de symboles 
Il convertit la sequence binaire de bits de duree Tb en une sequence de symboles de n bits de duree ts telle que ts = n.Tb 
**Le codage appelé M-aire, Ou M = $2^n$ correspondant au nombre de symbole différents**
Avec n le nombre de bits pour écrire 1 Symbole 

Tb = durée d'un bits 
Ts = durée d'un symbole 
Avec $T_s = n\;.\; T_b$ 

Si 4 symboles M=4 = 2^2 

R = 1 / Ts  → Débits de symboles en baud ou symboles 
D = 1/T → Débits binaire en bits/s

