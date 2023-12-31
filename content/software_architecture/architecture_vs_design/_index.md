+++
title = "Architecture VS Design"
weight = 10
+++

{{% notice style="tip" title="Ressources" icon="fa fa-book" %}}
- [Lesson 167 - Architecture vs Design](https://youtu.be/0tEBv2kAuNY)
- [https://stackoverflow.com/questions/704855/software-design-vs-software-architecture](https://stackoverflow.com/questions/704855/software-design-vs-software-architecture)
- [Chap3. - Java Application Architecture, Kirk Knoernschild](https://ptgmedia.pearsoncmg.com/images/9780321247131/samplepages/0321247132.pdf)
{{% /notice %}} 


Dans cette section nous étudierons la différence entre l'Architecture Logicielle (*Software Architecture*) et la Conception Logicielle (*Software Design*).
Il est important  de bien comprendre Les responsabilités d'un architecte celles d'un développeur ? 

> Penser comme un architecte, c'est connaître la différence entre l'architecture et la conception et comprendre comment les deux s'intègrent étroitement pour former des solutions.

## Définition
Wikipédia nous donne les premiers [élément de réponse](https://en.wikipedia.org/wiki/Architecture_description_language#Architecture_vs._design)

{{% notice style="warning" title=" " icon=" " %}}
La Conception Logicielle (*Software Design*) s'intéresse à l'implémentation concrète du code et à la mise en oeuvre des bonnes pratiques de programmation.
{{% /notice %}}

{{% notice style="warning" title=" " icon=" " %}}
L'Architecture Logicielle (*Software Architecture*) est un dégrès plus haut. On s'intéresse au partitionnement des grandes fonctionnalités, nous analysons les besoins métiers afin de s'assurer que les choix techniques vont pouvoir y répondre (extension, maintenance, performance, fiabilité, etc).
{{% /notice %}}

### Architecture Logicielle
L'objectif de l'Architecture Logicielle est de déterminer quel est le meilleur moyen de répondre aux besoins métiers. Elle répond au *quoi?*. On va déterminer les systèmes de stockage, la communication entres modules, les systèmes de récupération. On fait également des choix de technologie qui sont en adéquation avec les exigences techniques du client (maintenance, evolutilité, fiabilité, performance, etc ...).

On se concentre sur la stratégie à adopter. On va s'aider de patrons architecturaux (layered, event-based, microservices, etc) pour répondre besoins fonctionels et non-fonctionnels du client.

### Conception Logicielle
L'objectif de la Conception Logicielle est d'implémenter les exigences fonctionelles. Elle répond au *comment?*. Cette conception permet de se concentrer sur le fonctionnement interne de chaque module (e.g. classe Java), leur rôle et comment il va communiquer avec les autres modules. Elle nous aide à produire un code de bonne qualité en se basant sur les principes SOLID, les Design Patterns, etc ...

On se concentre sur l'implémentation concrète d'une architecture. Par exemple, nous regardons comment nous allons implémenter la logique métier `m` en utilisant l'Architecture Hexagonale.

## Etant donné que ...
Il est très compliqué de bien cerner la différence entre les deux, le mieux est de laisser les spécialistes du domaine apporter leurs éléments de réponse. Je vous conseille donc de lire les visions proposées par Marc Richard et Grady Booch.