+++
title = "Bounded Context"
weight = 10
+++

{{% notice style="tip" title= "Ressources" icon="fa fa-book" %}}
- [https://martinfowler.com/bliki/BoundedContext.html](https://martinfowler.com/bliki/BoundedContext.html)
{{% /notice %}} 

{{% notice style="warning" title= " " icon=" " %}}
Chaque service comprend tout ce qui lui est nécessaire pour fonctionner, classes, sous-composants, base de données.
{{% /notice %}} 

Un Bounded Context représente une limite spécifique et bien définie à l'intérieur de laquelle les termes, les concepts et les règles d'une logique métier sont définis et cohérents. Il s'agit d'un moyen de segmenter un système logiciel plus vaste en parties plus petites et plus faciles à gérer.

![Bounded Context](https://martinfowler.com/bliki/images/boundedContext/sketch.png?width=40pc)

## Granularité
La principale difficulté réside dans le fait de déterminer la bonne granularité pour un service. 

{{% notice style="note" title= "" icon="" %}}
Le terme *microservice* ne signifie pas qu'on doit faire des services les plus petits possibles.
{{% /notice %}} 

En effet, à cause du terme *micro* des personnes commettent souvent l'erreur de rendre leurs services trop petits, ce qui les oblige à établir des liens de communication entre les services pour effectuer un travail utile. Créer du lien c'est créer du couplage, créer du couplage montre une forte dépendante; pourquoi pas les réunir dans un seul et même service ?

Pour trouver les bonne frontière on peut suivre ces recommendations :
- Objectif : chaque service doit avoir une très forte cohésion fonctionelle. Contribuant à un comportement significatif de l'application.
- Transaction : les transactions posent des problèmes dans les architectures distribuées si on veut les éviter le mieux est de regrouper les services les partageant.
- Chorégraphie : si un architecte construit un ensemble de services qui offrent une excellente isolation, mais qui nécessitent une communication importante pour fonctionner, il peut envisager de regrouper ces services dans un service plus important afin d'éviter la surcharge de communication.

## Isolation des données
L'architecture microservices essaie d'éviter toute forme de couplace dont le partage de schemas de de base de données.

Par conséquent, chaque service devient responsable de sa source de vérité.