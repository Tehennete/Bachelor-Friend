---
aliases: 
Matière:
  - Technologie des Equipements
Semestre:
  - B2-2
Date: 2024-06-10
Prof: "[[François Fanelli]]"
Type: notes de cours
tags:
  - cours
---
# Enregistrement magnétique  
Date: [[2024-06-10]] 
  
### Généralités  
  
Méthode de mise en mémoire fondée sur les propriétés de certains matériaux à rester aimantés.  
Difficulté : permettre une restitution fidèle et précise des phénomènes enregistrés.  
L'enregistrement du son est à l'origine du développement de l'enregistrement magnétique depuis la fin du XIXème siècle. On trouvera ensuite des applications dans d'autres domaines comme la vidéo, l'informatique, l'audio-numérique…  
  
Historique  
  
• 1898 : Télégraphone, inventé par Valdemar Poulsen, enregistrement sur un fil de métal par un électro-aimant. (Ensuite apparition des tubes de puissance qui permettent des progrès)  
  
• 1927: Pfleumer couche des particules d'oxyde de fer sur du papier: Ancêtre de la bande magnétique.  
  
• 1928 : Stille enregistre sur un fil d'acier puis sur une bande magnétique  
  
• 1935 : AEG = Ier magnétophone à bande plastique et BASF = lère bande magnétique (6,3 mm de large) vendue en bobine.  
  
• 1947: Ampex commercialise aux USA un magnétophone aux très bonnes caractéristiques (bande passante 20 Hz - 18 kHz)  
  
• 1957 : premier 8 pistes AMPEX réalisé pour et à la demande de Les PAUL  
• 1961 : Philips invente la cassette audio (stéréo)  
  
• 1963 : Philips cède gratuitement son brevet sur le magnétophone  
  
• 1964 : Studer commercialise le J37, un 4 pistes sur bande 1/2 pouce qui servira à la réalisation de l'album des Beatles « Sergent Pepper»  
  
• 1908 : 3M (Modèle M 23) lance un magnétophone 8 pistes sur bande i pouce et Ampex lance un 16 pistes sur bande 2 pouces. Le premier magnétophone 8 pistes livré en Angleterre en 1968 était un SCULLY, aux Studios Abbey Road ce sera un 3M (Modèle M56)  
  
• 1970 : premier magnétophone 16 pistes en Angleterre  
  
• 1973 : Studer A8o - 24 pistes sur bande 2 pouces  
  
• 1976 : Olympus invente la micro-cassette pour dictaphone  
  
  
  
## Principes fondamentaux  
  
### Aimantation  
  
La magnétite, connue depuis l'Antiquité, exerce une force permanente d’attraction / répulsion appelée champ magnétique.  
L’oxyde de fer, ou l’oxyde de chrome s’aimantent quand il sont soumis à un champ magnétique. Lorsque le champ magnétique cesse, ces corps gardent une certaine aimantation qui sera utilisée ultérieurement pour la restitution du message d’origine.  
  
### Notion de magnétisme  
  
#### Champ magnétique :  
  
Désigne une région de l’espace soumise à l’action d’une force provenant d’un aimant  
Il est généralement noté B et son intensité se mesure en tesla (T)  
Exemple barreau aimanté : Voir cours  
Les pôles identiques se repoussent et les opposés s’attirent  
Loi de coulomb : force d’attraction de 2 corps de charge q et q’ espacés d’une distance d: F=k(q+q')/d2  
Avec q et q’ en coulomb, d en mètre, F en Newton et k constante qui dépend des unités.  
Important : Un courant électrique circulant dans un fil conducteur génère un champ magnétique induit noté H (B étant plus souvent utilisé pour le champ magnétique “naturel”)  
  
#### Induction magnétique  
  
Découverte par Farad, apparition d’une différence de potentiel aux bornes d’un conducteurs en mouvement dans un champ magnétique (micro dynamique et l’inverse pour le HP)  
de plus, si le conducteur et fixe mais le champ magnétique variable on a une différence de potentiel qui varie proportionnellement aux bornes du conducteur (c’est le principe de la tête de lecture du magnétophone). L’inverse fonctionne également (tête d’enregistrement).  
  
#### Flux d’induction magnétique  
  
Le flux noté  à travers une surface S plongé dans un champ magnétique B est donné par : =BS  
Il faut multiplier par cos() si B et S forment un angle  
  
#### Propriétés des corps ferromagnétique  
  
Courbe de 1ʳᵉ aimantation (bleu) : Lorsque l’on fait varier le champ magnétique) proximité d’un corps ferro magnétique comme l’oxyde de fer ou le dioxyde de chrome, on observe que l’aimantation prise par ce corps ne peut dépasser une valeur maximale appelée aimantation à saturation (Ms)  
Cycle d’hystérésis : On fait varier le champ magnétique H du positif vers le négatif et ainsi de suite. On observe en parallèle l’évolution de l’aimantation M reçue par le corps.  
Après la première aimantation et que la saturation est atteinte (Ms) on fait diminue H alors m diminue suivant la courbe en rouge. Lorsque le champ H passe par la valeur O, l'aimantation garde une valeur appelée aimantation rémanente après saturation (+ Mr). Pour une bande magnétique, cette valeur doit être la plus grande possible, par contre elle doit être pratiquement nulle pour une tête magnétique !  
  
Si on inverse le champ H, l'aimantation s'annule pour la valeur -Hc (champ coercitif). Si H diminue encore, on arrive à un minimum de saturation pour l'aimantation (-Ms) et si on repart vers un champ positif, on passe par la valeur -Mr pour H=o puis par la valeur M=o  
pour H = +Hc. Enfin on repasse par M-Ms pour un champ H=Hs.  

>[!note]
> On peut décrire des cycles partiels, il s'agit de faire varier H (+ et -) sans atteindre les valeurs de saturation de M. Ainsi il est possible d'arriver à M=o (démagnétisation complète) en faisant varier H (+ et -) tout en diminuant lentement l'amplitude. Ce principe est parfois utilisé pour démagnétiser un magnétophone.  
  
## Technologie  
  
### Bandes magnétiques  
  
Support initialement en papier puis acétate de cellulose et enfin polyester recouvert d’oxyde de fer ou le dioxyde de chrome fixé par un liant (résine)  
Elle défile à différentes vitesses devant les têtes du magnétophone (19,38 ou 47 cm/s)  
La largeur de la bande définit le nombre de pistes ( de 1 à 24) qu el’on pourra enregistrer. On trouve les largeurs suivantes : ¼”(1 ou 2 pistes),½” (pistes),1”(8 pistes),2”(16 ou 24 pistes)  
L’épaisseur est de 50µm  
  
### Les têtes magnétiques  
  
C’est un circuit magnétique en forme d’anneau coupé par un entrefer étroit. L’entrefer est obtenu par l’intersection d’une cale de matériau non magnétique. Elle est normalement placée perpendiculaire à la bande magnétique.  
Effacement (DEL): Parcourue par un signal alternatif qui produit un champ magnétique décroissant qui amène les particules de la bande dans un état neutre  
Enregistrement (REC): Produit un champ magnétique en fonction du signal audio qui aimante les particules d’oxyde de la bande  
Lecture (Play): capte et transforme le champ magnétique présent sur la bande en signal audio électrique  
  
### Effacement  
  
têtes avec un entre fer large  
Courant alternatif de haute fréquence  
EN passant devant l’entre fer, la piste subit de nombreuse alternances de champ magnétiques qui décroit lorsque la bande défile  
Effacement de bonne qualité si l’intensité du magnétique est suffisant pour saturer l’oxyde de fer et si la décroissance est progressive. L’aimantation tend vers 0.  
  
### Enregistrement  
  
EQ: Elle est appliquée au signal avant l’enregistrement, elle suit une courbe standardisée en fonction des vitesses de défilement, car en lettre le niveau de sortie augmente avec la fréquence.  
  
Polarisation : Les caractéristiques d’aimantation d’une bande ne sont pas linéaires ainsi on superpose au signal audio un signal sinus de très HF qui polarise l’oxyde de fer  
  
Echo magnétique :Il est créé une zone enregistrement sur la bande qui induit un champ magnétique…   
  
  
### Lecture  
  
filtre coupe bas -> EQ->Amp -> Effet d’entre fer  
  
  
Positionnement des têtes  
  
Effet d’azimut  
Effet d’auteur  
Effet d’éloignement  
Effet de zénith  
  
  
  
  
  
3) Les normes  
  
Niveaux enregistrement  
  
C’est le niveau d’aimantation de la bande, en nWb/m  
Niveau de saturation de la bande  
Niveau 0 de magnétisation, c’est le niveau de référence de magnétisation de la bande ( idem que le niveau nominal)