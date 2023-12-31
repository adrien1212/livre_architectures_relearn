+++
title = "Solution"
weight = 10
+++

{{% notice style="tip" title="Ressource" icon="fa fa-icon" %}}

- [https://thevaluable.dev/cohesion-coupling-guide-examples/](https://thevaluable.dev/cohesion-coupling-guide-examples/)
- [https://enterprisecraftsmanship.com/posts/cohesion-coupling-difference/](https://enterprisecraftsmanship.com/posts/cohesion-coupling-difference/)
  {{% /notice %}}

{{% notice style="warning" title=" " icon=" " %}}
L'objectif est de respecter le principe " _Low coupling, High cohésion_ "
{{% /notice %}}

## Concepts liés

Le _couplage_ et la _cohésion_ sont liés :

- Si vous avez une bonne cohésion dans votre module, tout les éléments sont couplés.
- Si tout ce qui va ensemble est ensemble, changer le module n'affectera pas les autres modules.
- Si changer quelque chose dans le module A affecte le module B, cela signifie que cette chose du module A devrait être dans le module B.

## Comment achever Low coupling, High cohésion

> To achieve less coupling, each module should know the minimum about each other

Pour ce faire, nous devons introduire des abstractions. Cette abstraction (i.g. une interface en Java) doit expose uniquement les fonctionnalités nécessaires pour d'autres module; ni plus ni moins. Ceci offre plusieurs avantages

- vous aurez un modèle clair, une représentation claire de votre base de code. Il sera plus facile de le modifier et de le maintenir.
- Différentes équipes peuvent travailler sur différentes parties de la base de code, sans se marcher sur les pieds. Si les modules de haut niveau ont une forte cohésion et un faible couplage, la modification d'un module n'affectera pas les autres.
- Utiliser une partie de votre base de code sur une autre.
