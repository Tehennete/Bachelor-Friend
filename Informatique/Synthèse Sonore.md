---
Matière: Informatique
Semestre: B2-1
Date: 2023-11-09
Prof: "[[Olivier Stalla]]"
Type: notes de cours
tags:
  - cours
  - Informatique
---
# Synthèse Sonore
Date: [[2023-11-09]] 
## Différents types 
Additive
Soustractive 
FM
Granulaire

## Théorème de Fourier
Décomposition de la série naturelle des Harmonique. 

| 1           | 2      | 3      | 4      | 5      | 6      | 7             | 8      | 9             | 10     | 11                  | 12     |
| ----------- | ------ | ------ | ------ | ------ | ------ | ------------- | ------ | ------------- | ------ | ------------------- | ------ |
| 100Hz       | 200Hz  | 300Hz  | 400Hz  | 500Hz  | 600Hz  | 700Hz         | 800Hz  | 900Hz         | 1000Hz | 1100Hz              | 1200Hz |
| Fondamental | Octave | Quinte | Octave | Tierce | Quinte | Septieme min. | Octave | Neuvième Maj. | Tierce | Quarte aug (fausse) | Quinte | 
![[Pasted image 20231109133340.png]]

Hauteur = Fréquence
Timbre = 
Intensité = 
### Théorème de Fourier 
Tous les sons complexes (avec des harmoniques) périodiques peuvent se décomposer en une somme de sons pures (qui n'ont aucune harmonique) dont les fréquences sont des multiples entiers de la fréquence la plus basse. 
On peut utiliser les harmoniques suivante d'une note pour donner la sensation que le fondamentale est présent sans jouer le fondamental.

## Synthèse additive 
L'orgue Hamon, ou on ajoute les fréquences petits à petits. LA plus part des synthés à synthèse additive ont disparu aujourd'hui (regarder Casio). 

## Synthèse Soustractive 
On fournit un son très riche que l'on va ensuite filtré, chaîne classique d'une synthèse soustractive. 
**VCO** (Voltage Control Oscillateur) → **VCF** (Voltage Control Filter) → **VCA** (Voltage Control Amplifier) Parfois avec une enveloppe → Suite de la chaîne sonore. 
**LFO** (low frequency oscillateur) qui va moduler les éléments du synth. 
Souvent dans les synthé tu as deux VCO. 

#### VCO 
Type standards de génératrice de signal que l'on trouve dans un synthé classique
Signal type SIN = le fondamentale 
Signal type SAW = toutes les H 
Signal type SQR = Toutes les H impaires : son 1, son 3(quinte), son 5(tierce), son 7(septième min) (son basé sur les quinte)
Signal PW (pulse Width → La largeur du carré)
Signal triangle  = Harmoniques Paire atténuées 

On peut mettre une enveloppe sur le VCO

#### VCF
Souvent un LPF 
Avec pour fréquence de coupe : Cutoff
Et une résonance 
![[Pasted image 20231109142159.png|600]]
Une slope pour faire varier la pente du filtre. 
6/12/18/24… 
On peut mettre un générateur d'enveloppe sur le VCF

>[!NOTE]
>Enveloppe ADSR 
> Attack(temps) - Decay(temps) - Sustain (%) - Release(temps)
> Sustain n'est pas une temporalité mais un entretien de la note, c'est le temps ou le joueur reste appuyé sur la touche

#### LFO 
Il y a aussi des formes d'ondes
SIN - 
SAW - 
SQR - 
RANDOM - 