---
Matière: Technologie des Equipements
Semestre: B2-1
Date: 2023-10-12
Prof: David Laurent
Type: notes de cours
---
# Les Normes PAD
Date: [[2023-10-16]] | Tags : #cours 

>[!NOTE]
>Étude de l'évolution et des recommandations actuelles concernant les nomes PAD (Prêt à Diffuser) principalement dans le domaine de l'audio-visuel et de la diffusion télé et plateforme de streaming. La mesure Loudness fera l'objet d'une étude approfondie
## Introduction
### 1 Définition
**PAD** : Prêt A Diffuser, norme technique imposée en fonction de critères stricts par les diffuseur (chaîne de TV, plateforme de streaming…). Elles concernent l'image et le son, et doivent être respectées scrupuleusement pour que le projet soit considéré comme diffusable. Si elles ne sont pas respectées (surtout en tv), le projet sera renvoyé. C'est rédibitoire.

**Loudness** : Mesure *moyenne et subjective* d'un programme avec plusieurs critères dans le but

**ITU-R BS.1770-1** : Norme Loudness internationale initiale

La **CST** (Commission Supérieure des Techniques de l'image et du Son) a établi des recommandations pour les programmes to en 2011 (CST_RT_017_TV_V3)

**EBU R128** : Norme Loudness TV en vigueur au niveau européen issue des recommandation de la CST (la version *R128 S2* d'applique au streaming et ma *R128 S3* à la radio). C'est cette norme que l'on doit respecté actuellement.

La chose la plus complexe de notre métier, c'est la transposabilité de notre travail. Un bon mix/master sonne bien sur tous les supports. En musique comme en audio-visuel.

Ces normes on permis la naissance de nouvelles boites de "délivery", pour livrer des mix/master diffusables sur les différentes plateformes. Donc c'est faire des versions adaptés techniquement à chaque support et normes.
### 2 Historique
Avant 2011, les normes de mixage pour une diffusion TV étaient peu exigeantes : Niveau d'alignement - 18dBFS et Peak maximal -9 dBFS

Cela a mené à de grande disparités dans le rendu sonore des programmes : la tendance fut de maximiser le niveau sonore avec forte compression en poussant le mixage vers le niveau maximum autorisé.

Les recommandations (CST-RT 017) et normes actuelles (EBU R128 ou ITU R BS-1770) ont été mises en oeuvre pour stopper cette dérive et proposer une écoute homogène et qualitative au téléspectateurs. 

## Loudness et Normes 
### 1 Mesure Loudness 
La mise en place de la mesure Loudness, basée sur la perception et le ressenti sonore vise **à garantir un confort d'écoute, une bonne intelligibilité et une continuité homogène dans l'enchaînement des programmes, tout en respectant les choix artistiques des oeuvres diffusées.** 
La mesure Loudness des programmes nécessite une méthode spécifique avec plusieurs critères d'analyse (mesure à court terme, moyenne sur l'ensemble, dynamique, niveau maximal instantané)

Une échelle spécifique est définie : LU (Loudness Unit) Et LUFS (Loudness Unit relative à une échelle dBFS), si on fait +1 sur une échelle LUFS, ça correspond à +1dBFS.

Plusieurs institutions internationales ont proposé des normes qui se rejoignent sur certains points :
- *Europe* : EBU R128
- *USA* : ATSC A/85 RP
- *International* : ITU-R BS.1770-1/ évolue en 2, 3, 4 (Dernière en vigueur)  (avec LKFS, où la mesure ce fait avec une courbe de pondération K, à regarder si c'est encore présent sur la dernière version)

>[!info] Remarque
>	La CST a proposé des recommandations qui sont reprises par certains diffuseurs to en France = Recommandation CST-RT-017-V3 (très ressemblante à la norme EBU)
 
Donc il faut aller voir sur les normes PAD de la chaîne quelle norme elle applique et ses recommandation techniques. (Fiche PAD quoi).
### Les critères de mesure
Tout d'abord un filtre coupe bas (à 100Hz) est appliqué ainsi qu'un filtre shelving d'augmentation de +4dB à partir de 1500Hz (pour tenir compte des effets acoustique de la tête). On parle d'une courbe de pondération K

![[IMG_0022.jpeg]]

Ensuite on applique un "safety" gate avec un seuil à -70dBFS pour éviter de mesurer les niveaux trop faibles ou les silences qui ne sont pas représentatifs du ressenti. Et dans certains cas un autre gate dont le seuil est variable se situant 10 LU en dessous de la valeur moyenne mesurée (integrated ou long term)

#### Loudness cible (Target Loudness) / en LUFS
Valeur à atteindre pour le loudness moyen à la fin du programme ou de la mesure 
#### Loudness Integrated ou Long Term ou Infinite / en LUFS
C'est la mesure de loudness faite sur une longue période. Impliqué un start/stop pour définir la mesure. Utilisé en général pour obtenir **la Moyenne sur la durée totale du programme**
#### Loudness Short Term / en LUFS
C'est une mesure de loudness qui intègre les 3 dernières secondes (défini par EBU). Un Meter Short Term affiche le **niveau moyen des 3 dernières secondes**. Il donne une idée de l'évolution du niveau du programme et de sa dynamique. Le loudness Short Term est mesuré sans la "Safety" gate. 

> [!note] Notabene
> certains instruments de mesure permettent aussi un short term sur 10sec.

#### Loudness Momentary / en LUFS
C'est une mesure de loudness (sans gate) **intégrée sur 400ms** (définition EBU). Sert de "Vu-mètre" agrémenté de la pondération ITU. Peu utilisé actuellement. Unité = LUFS

> [!note] Notabene 
> La norme ITU utilisait la notation LkFS pour signifier que la courbe de pondération k était appliquée. Aujourd'hui une harmonisation autour de l'unité LUFS a été mise en place 

#### True Peak / en dBTP
C'est une **mesure instantanée des pics** de signal en tenant compte l'évolution du signal entre 2 échantillons. Elle peut être plus élevée (ou plus faible) que sa valeur crête la plus élevée d'un échantillon. Les instruments de mesure sur-échantillonent 4x, ce qui permet de mesurer en True Peak. Les autres types de mesures peuvent sous-évaluer le niveau du signal, spécialement dans les hautes-fréquences.

- ![[IMG_0023.png]]

Ci-dessus en rouge la ligne haute c'est le true peak, la ligne qui passe sur l'échantillon c'est le dBFS.

#### Loudness Range (LRA) / en LU
Cette mesure quantifie l'aspect dynamique du programme. Elle se base sur la mesure Short Term 3s avec un filtre et gate fixe à -70 LUFS et un gate relatif à -20 du niveau pour évacuer le bruit de fond de la mesure. (Le seuil du deuxième gâte fluctue en étant toujours à -20 du niveau)

On ne prend en compte que les données situées entre le 10ème et le 95ème centile. On ne conserve que les signaux utiles (des signaux les plus faibles - hors bruit de fond - aux signaux les plus forts - hors bruits forts ponctuels). 

Le LRA c'est une sorte de moyenne du niveau de la dynamique. C'est une mesure représentative du niveau sonore sur l'ensemble du film. 

![[Les Normes PAD 2023-10-16 11.08.08.excalidraw]]
Les 10% les plus faibles sont pris en fonction de la gate relative. Sur le schéma la courbe représente la quantité de niveau présent sur l'ensemble film.
C'est donc basé sur le short term mesuré sur l'ensemble du film. On regarde sur combien de pourcentage du temps ce niveau est présent. C'est des statistiques.
Le gate relatif ce fait pendant les statistiques. 

Il marche en continue (les statistiques sont instantanées).

Pour le faire en rendu, on peut utiliser le plug d'analyse en audio suite.

Mais quand on mix c'est avec nos oreilles qui nous guident, et donc il faut bien régler le niveau de sortie. 

### 3 Norme ITU-R BS 1770
lle définit les méthodes et les algorithmes de mesures du Loudness. (Pondération K, Gate, mesure, true Peak…)
### 4 Norme EBU R128 (TV)
En vigueur en Europe :  
- Basée sur les mesures de l'ITU-R BS.1770-2
- Propose d'unifier les unités LUFS et LKFS
- Niveau cible : -23 LUFS
- Niveau crête : -1 dBTP
- Mesure du LRA (en LU) : Entre 0 et 2, conseillé 5-20 (un talk-show sera proche de 5 tandis qu'un film sera plutôt autour de 17)
### 5 Recommandations CST-RT-TV-017-V3
De nombreux diffuseurs TV en France se basent sur ces recommandations.
- Basée sur l'EBU R128
- Long term = -23LUFS avec tolérance + ou -1 si ppm > à 2 minutes
- Short Term (3sec) dial = + ou -7 autour de -23/
- LRA max = 20 LU
- True Peak = -3dBTP (peut varier selon les chaînes)
Tableau des valeurs recommandées par la CST

![[IMG_0025.png]]