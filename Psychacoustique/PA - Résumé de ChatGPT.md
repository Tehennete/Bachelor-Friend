---
aliases:
Matière:
  - Psychoacoustique
Semestre:
  - B2-1
Date: 2024-01-18
Prof: "[[Laurent Allard]]"
Type: notes de cours
tags:
  - cours
  - Psychoacoustique
---
# PA - Résumé de ChatGPT
Date: [[2024-01-18]] 

D'accord, je vais essayer de vous faire une synthèse un peu plus détaillée du phénomène de propagation guidée des ondes acoustiques dans un tube de section constante S. Voici ce que je vous propose :

- Le son est une vibration de l'air, qui fait varier la pression et le déplacement des molécules d'air. Quand vous soufflez dans un tube rempli d'air, vous créez une onde acoustique qui se propage dans le tube.
- Cette onde acoustique est décrite par deux fonctions : la pression $p(x,t)$ et le déplacement acoustique $s(x,t)$, qui dépendent de la position $x$ dans le tube et du temps $t$. Ces fonctions sont reliées par deux équations, qui viennent des lois de la mécanique et de la thermodynamique :
    - La première équation dit que la variation de pression est proportionnelle à l'accélération du déplacement acoustique, avec un coefficient qui est la masse volumique de l'air $\rho$ :

    $$\frac{\partial.p}{\partial.x}=-\rho\frac{\partial^2s}{\partial.t^2}$$

    - La deuxième équation dit que la variation de déplacement acoustique est proportionnelle à la pression, avec un coefficient qui est le coefficient de compressibilité de l'air $\chi_s$ :

    $$\frac{\partial.P}{\partial.x}=-\rho\frac{\partial^2s}{\partial.t^2}$$

- Pour résoudre ces équations, on fait quelques hypothèses simplificatrices : on suppose que le tube est infini, ou que ses extrémités sont fermées par des parois rigides ; on suppose que le tube a une section constante S, et que l'air est homogène et isotrope ; on suppose que les variations de pression et de déplacement acoustique sont petites devant les valeurs moyennes.
- Avec ces hypothèses, on peut chercher des solutions de la forme :

    $$p(x,t) = p_0 + p_1 \cos(\omega t - kx + \phi)$$

    $$s(x,t) = s_0 + s_1 \cos(\omega t - kx + \phi)$$

    Où $p_0$ et $s_0$ sont les valeurs moyennes de la pression et du déplacement acoustique, $p_1$ et $s_1$ sont les amplitudes des variations, $\omega$ est la pulsation, $k$ est le nombre d'onde, et $\phi$ est la phase.

- Ces solutions sont des ondes planes, qui se propagent dans le tube avec une direction fixe. Elles sont caractérisées par les paramètres suivants :
    - La fréquence $f = \frac{\omega}{2\pi}$, qui mesure le nombre de vibrations par seconde de l'onde.
    - La longueur d'onde $\lambda = \frac{2\pi}{k}$, qui mesure la distance entre deux crêtes de l'onde.
    - La vitesse de phase $v_\phi = \frac{\omega}{k}$, qui mesure la distance parcourue par l'onde en une seconde. Elle est constante et indépendante de la fréquence, et elle vaut :

    $$v_\phi = \frac{1}{\sqrt{\rho \chi_s}}$$

    - L'amplitude de pression $p_1$, qui mesure la différence de pression entre le maximum et le minimum de l'onde. Elle est en opposition de phase avec le déplacement acoustique, et elle vaut :

    $$p_1 = -\frac{\chi_s}{\rho} \omega^2 s_1$$

    - L'amplitude de déplacement acoustique $s_1$, qui mesure la distance maximale parcourue par les molécules d'air.

- Ces ondes planes sont appelées **modes propres** du tube. Il y a une infinité de modes propres possibles dans le tube, mais certains sont plus faciles à produire que d'autres. Par exemple, le mode propre le plus bas, c'est celui qui a la fréquence la plus basse, la longueur d'onde la plus grande, la vitesse de phase la plus élevée, l'amplitude de pression la plus faible et l'amplitude de déplacement acoustique la plus forte. C'est le mode fondamental du tube. Les autres modes propres sont des harmoniques du mode fondamental, c'est-à-dire qu'ils ont des fréquences multiples de la fréquence fondamentale.

- Quand vous soufflez dans le tube, vous pouvez créer un seul mode propre, ou une combinaison de plusieurs modes propres. Le son que vous entendez est le résultat de cette combinaison. Si vous changez la façon dont vous soufflez, vous pouvez changer les modes propres que vous créez, et donc changer le son que vous produisez.

Voilà, j'espère que cette synthèse un peu plus détaillée vous a permis de comprendre le phénomène de propagation guidée des ondes acoustiques dans un tube de section constante S. Si vous voulez approfondir le sujet, vous pouvez consulter les sources que je vous ai données dans ma première réponse. Si vous avez d'autres questions, n'hésitez pas à me les poser. 😊