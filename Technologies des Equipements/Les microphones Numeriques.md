---
aliases: 
Matière:
  - Technologie des Equipements
Semestre:
  - B2-2
Date: 2024-05-16
Prof: "[[David Laurent]]"
Type: notes de cours
tags:
  - cours
  - "#flashcards-te"
---
# Les microphones Numeriques
Date: [[2024-05-16]] 

Objectif 
Étude de la technologie des microphones numériques (Majoritairement Electrostatiaues) et les caractéristiques techniques 

### Introduction / rappel 

Le microphone

Introduction/ Rappels:

Le microphone est un transducteur qui convertit l'énergie acoustique en énergie électrique. Le signal obtenu est un signal analogique.

Un convertisseur Analogique/Numérique (CAN ou ADC en anglais) consiste à mettre un signal analogique sous la forme d'une suite de nombres binaires. Cette opération se réalise en 2 étapes:

- L'échantillonnage: On prélève un nombre régulier d'échantillons par seconde sur la courbe analogique (= Fech de base 44,1 kHz pour le CD Audio et 48 kHz pour l'Audiovisuel Broadcast).

- La quantification: La mesure de l'amplitude de chaque échantillon est transformée en valeur binaire de 16 ou 24 bits., ce qui offre un dynamique théorique de 96 ou 144 dB.

Ces processus nécessitent un cadence rigoureuse donnée par un signal d'horloge interne ou externe appelée Word Clock, qui doit être commun à toutes les machines d'une chaîne d'appareils numérique.

Les conversions A/D et D/A successives tout au long d'une chaine dégradent le signal, il est donc recommandé de convertir le plus tôt possible et de rester en numérique le plus longtemps possible.

Ainsi la conception de micros numériques a pour objectif de convertir plus tôt dans la chaîne du son, de conserver la dynamique des micros statiques et garantir un bruit de fond très faible.

## Principe de fonctionnement / Exemples

### Généralité 
Un micro numérique consiste en une association de technologies existantes : 

> Micro + Préamplificateur + Convertisseur A/N 

- Un micro statique possède une dynamique d'environ 130dB, il faut privilégier une quantification en 24bits (144dB dynamique théorique) pour en profiter pleinement. 
- Un CAN ne peut convertir que des signaux niveau LINE (environ 1 V), or la sortie d'un micro est beaucoup plus faible (quelques mV), il sera donc nécessaire d'intégrer un préamplificateur micro dans les circuits du micro numérique ou d'adapter les convertisseurs.
- Un micro statique a besoin d'une alimentation pour fonctionner (alimentation fantôme + 48 V en analogique). Il faudra donc prévoir une technologie d'alimentation pour les micros numériques pour la partie micro, le préamplificateur et le CAN). Il s'agit de l'alimentation **DPP (Digital Phantom Power)** dont la valeur est + 10V / 250mA. Uniquement présente pour ce type de micro. 
- Le Word Clock doit être envisagé en maître ou en esclave pour les différentes configurations.

Caractéristiques de la mémoire DDP :: digital phantom power +10V / 250mA
### Beyerdynamic série MCD

- Premier constructeur à avoir commercialisé un micro numérique en 1999
- Directivité Fixe 
- Gain fixe ou variable avec boîtier externe uniquement.
- Sortie AES3 avec un seul canal 
- Boîtier spécifique (qui permet l'alimentation du micro et son contrôl)
- Technologie sortie trop tot, pas de réussite commerciale. 

### Neumann Solution-D
- micro numérique D-01 + boîtier externe interface DMI + logiciel RCS 
- Sortie en 2003 
- Micro 
2 convertisseurs A/N (un pour les niveaux bas et l'autre pour les niveaux forts). Ce qui permet de ne pas à avoir à régler le gain analogique.
- Statique double membrane = directivitéC variable 
- Horloge interne word clock (Async) ou mode Slave par boîtier externe (Sync). 
- **Interface DMI-2 portable** 
	- 2 entrées AES42 
	- 1 sortie AES3 
	- USB pour connection ordi + logiciel 
	- BNC word clock in / out 
	- Il fournit l'alimentation DPP
	- Permet de télécommander les différents fonctions présentes dans le micro (gain numérique, choix de directivité,…, coupe bas, limiteur …)
- Logiciel RCS (Remote Control System)
	- Assure le contrôle à distance des fonctionnalités du micro 
	- Choix des directivités, coupe bas, gain, synchro word clock (Async ou sync), Choix Fech, limiteur, monitoring des niveaux en dBFS
>[!note]
>D'autres references de micro numériques Neumann : TLM 103D, KM184D, KMS105D, KMR81D

Chez Schopenhauer : Le CMD 2U et le superCMIT (canon directivité de 2ème ordre interessant mais il n'est pas synchronisable)
Chez Sennheiser : MKH 8020/8040/8050. Les modules canons MKH 8060 et 68070. Le MZD 8000 pour MKH 8000

## AES 42 
### Câblage 
Idem à celui de l'AES 3 : Paire torsadée + masse, impedance 100ohms 
### Connectique 
Connecteur XLR 3 points 
Connecteur XLD : 
- Connecteur format XLR avec une rainure placée entre les points 2 et 3
- Possibilité d'insérer une clé de codage qui empêche la liaison XLR - XLRD
- Bague de repérage optionnelle à traits blancs 
### Alimentation 
- DPP : Digital Phantom Power 
- +10V
- 250mA 
- Elle est générée et envoyée au micro par le boitier d;interface externe ou par la console numérique via la liaison AES42 
### Données audio 
Idem à l'AES3 
Utilisation des bits C et U des sous-trames pour coder des retours d'infos de télécommande. 
### Telecommande
Impulsions codées de 2V transmises au micro depuis le boitier externe (directement ou via logiciel). Ces impulsions sont ajoutées à l'alimentation DPP sans la perturber. 
Débits = 750kbits/s à 48kHz (32 instructions/s)

### Synchronisation 
2 modes proposés : 
- mode 1 : Le micro sera **MASTER**. Tous les appareils doivent être synchronisés avec l'horloge interne du micro via la liaison AES 3. Ce mode fonctionne si on utilise un seul micro numérique. Si on utilise plusieurs micros dans ce mode, il faudra activer le circuit SRC (Sample Rate Converter) de la console numérique. Ce qui peut induire de la latence et une degradation du signal 
- Mode 2 : Le micro sera en Mode **SLAVE**. L'horloge word clock utilisée par le micro celle de la console numérique (ou autre) **reliée au Word Clock In du boitier externe**.

## Conclusion
- Les avantages principaux sont 
	- Chaîne complete de travail numérique possible excellent rapport signal/bruit 
	- Grande plage dynamique sans risque de saturation
	- Meilleur definition du son. Couleur quasi identique à celle d'un micro analogique, mais avec plus de details 
	- Pas besoins de preamp micro ni de convertisseur A/D

-  Les inconvénients principaux sont :
	- La mise en oeuvre des micros numériques nécessite quelques précautions particulières et parfois des équipements complémentaires (boitier interface, ordi, logiciel...) pour bénéficier de toutes leurs fonctionnalités.
	- Le cout de ces dispositifs est relativement élevé.
	- Les micros numériques consomment beaucoup d'énergie ce qui restreint pour le moment les utilisations nomades ».
	- L'utilisation avec des émetteurs HF Numériques est limitée (il existe un émetteur avec entrée AFS42 chez Zaxcom).
	- La pertinence de l'apport qualificatif au regard des contraintes et par rapport à d'excellents micros et appareils analogiques est sons doute encore discutable. 
	- Nous trouverons done ce genre de micros dans des configurations très exigeantes qualitativement, avec des besoins de bruit de fond très faible et de grande dynamique, avec des moyens financiers de production importants. Ainsi il n'est pas surprenant de voir ces micros utilisés principalement dans certains studios d'enregistrement haut-de-gamme et dans le domaine de la musique classique. Les fabricants comme Neumann espèrent à l'avenir intégrer le marché de la tv et du cinéma avec cette technologie.