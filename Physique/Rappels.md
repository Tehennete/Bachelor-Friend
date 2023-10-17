---
Matière: 
Semestre: 
Date: 2023-10-12
Prof: 
Type: notes de cours
tags:
  - cours
---
# Sans titre
Date: [[2023-10-17]] 

## Atténuation géométrique
### Cas 1
![[Rappels 2023-10-17 10.07.12.excalidraw|300]]
$L_{loin}=L_{proche}-20.log(\frac{d1}{d2})$
### Cas 2
![[Rappels 2023-10-17 10.10.55.excalidraw|300]]
#### 1ère méthode
 1. D'abord : $I_2 = Q .\frac{W}{4\pi.d_2^2}$
 Avec Q = facteur de directivité
 2. $L_{Loin}= 10.log(\frac{I_2}{I_{ref}})$
#### 2ème Méthode 
$$L_{loin} = L_W - 20 log(d2) - 11 +ID$$

ID = Indice de directivité → ID = 10log(Q)
##### Démonstration du +11
Soit $I_2 = Q. W/4\pi.d_2^2$
Niveau sonore : $L_{loin}=10log(\frac{I_2}{I_{ref}})$
$=10log(\frac{Q.W}{I_{ref}.4.\pi.d_2^2})$
donc 
$L_{loin} = 10.log(Q)+10.log(\frac{W}{I_{ref}})-10.log(4\pi)-10.log(d_2^2)$
$= ID +L_W - 11 - 20.log(d_2)$
## Addition de plusieurs sources
Il y a deux cas : avec les sources non-corrélée et les sources corrélées
### Sources non-corrélées
#### Cas 1 
On a n sources différents avec pour niveaux : $L_1, L_2, L_3, L_n….$
$$L_{tot} = 10.log(10^{\frac{L_1}{10}}+10^{\frac{L_2}{10}}+10^{\frac{L_n}{10}}+....))$$
#### Cas 2
Quand on a n sources identique de niveaux $L_1=L_2=L_3=…=L_n$
$$L_{tot}= L_1+ 10.log(n_{nb-sources})$$

Par exemple pour deux sources : $L_{tot}= L_1 + 3$

### Sources Correlées

#### Cas 1 
On a n sources différents avec pour niveaux : $L_1, L_2, L_3, L_n….$
$$L_{tot}= 20.log(10^{\frac{L_1}{20}}+10^{\frac{L_2}{20}}+10^{\frac{L_n}{20}}+....))$$
#### Cas 2 
Quand on a n sources identique de niveaux $L_1=L_2=L_3=…=L_n$
$$L_{tot}=L_1 + 20log(n)$$
Exemple pour 2 source $L_{tot}= L_1 + 6$