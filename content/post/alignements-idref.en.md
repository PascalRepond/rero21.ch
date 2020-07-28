---
title: "Migrations et crise d'autorités : les alignements IdRef"
date: 2020-07-28T15:10:18+02:00
publishdate:
draft: false
tags: ["autorités", "métadonnées", "data-alignment", "idref", "rero-ils", "slsp"]
---

La migration prochaine des données de {{< smallcaps "rero" >}} dans [(SLSP)][1] et {{< smallcaps "rero ils" >}} implique de traiter non seulement des notices bibliographiques, mais également des notices d'autorité. Les catalogueurs et catalogueuses du réseau en ont entré plus de 2.5 millions au fil des années. Qu'adviendra-t-il de cette précieuse base de données à l'horizon 2021 et quel traitement doit être entrepris ? Etienne Attinger s'est penché sur ces questions dans le cadre d'un travail de Bachelor en information documentaire mandaté et suivi par {{< smallcaps "rero" >}}.

<!--more-->

## IdRef, le futur des autorités

Fruits d'un travail de catalogage et d'indexation de longue haleine, les autorités de {{< smallcaps "rero" >}} sont un enjeu de taille pour toutes ses bibliothèques et leurs usagers, quel que soit le nouveau système auxquels ils sont destinés. Dans ce contexte, ces notices d'autorité seront intégrées dans l'application [(IdRef)][2]. Ce système développé par l'[(Abes)][3] est un référentiel d'autorités francophone ouvert mettant l'accent sur l'interopérabilité des données. 

L'avantage de ce type d'application est de décloisonner les catalogues d'autorités grâce à la puissance du web. En pratique pour un·e bibliothécaire, plutôt que de pomper obligatoirement une autorité-auteur depuis une base fermée, il lui sera possible de lier un document à des autorités externes venant par exemple d'[(IdRef)][2] ou de la [(GND)][4]. Le catalogue choisi importe peu tant que l'entité abstraite _personne_ est correcte. Dans ce cadre, le projet [(VIAF)][5] qui a pour but d'aligner internationalement les autorités de nombreuses bibliothèques est une aide préciseuse.

L'objectif des bibliothèques de {{< smallcaps "rero" >}} est donc d'aligner leurs autorités avec celles déjà présentes dans IdRef afin de les y intégrer d'ici fin 2020 évitant au maximum les erreurs, doublons et pertes. L'enjeu est celui de la conservation d'un travail long de plusieurs décennies fait par tous·tes les professionnel·le·s ayant travaillé sur les autorités du catalogue {{< smallcaps "rero" >}}. Du reste, un certain nombre de ces notices sont d'importance régionales et/ou patrimoniales.

## Analyse des données

Le travail d'Etienne Attinger avait pour but d'évaluer et analyser des données fournies par l'Abes et résultant d'alignements automatiques, afin de définir et documenter les traitements et vérifications manuels requis avant la migration des données. Ce travail est impératif pour limiter l'insertion d'erreurs et autres doublons dans le référentiel IdRef.

Les tests d'alignement ont débuté à l'Abes sur des échantillons fournis par {{< smallcaps "rero" >}} : d'abord 10'000, puis 80'000, et enfin 200'000 notices. Ces données ont été comparées par machine à celles d'IdRef en plusieurs fois via un logiciel interne dédié nommé _QE_ (prononcer "key") : 
- Une première comparaison se fait entre les données de {{< smallcaps "rero" >}} et celles d'IdRef
- Une seconde comparaison avec les données de VIAF permet d'améliorer et consolider les premiers résultats
- Enfin, les alignement VIAF entre les autorités {{< smallcaps "rero" >}} et celles de la BnF sont à leur tour utilisées pour comparer les données et aligner le plus d'autorités possibles

L'Abes a ensuite fourni à {{< smallcaps "rero" >}} des fichiers contenant les conflits, doublons et autres incertitudes à résoudre manuellement. Malgré l'efficacité impressionnante du traitement logiciel de ces alignements par l'Abes, environ 2.3% des autorités doivent encore bénéficier d'un travail manuel de vérification afin d'être pleinement validées. La pratique habituelle de {{< smallcaps "rero" >}} de n'indiquer les dates de vie d'un auteur qu'en cas de doublon interne s'est révélée être un handicap, parmi d'autres, pour ce travail d'alignement.

## Quel travail concret ?

Dans l'idéal, les bibliothécaires du réseau devraient vérifier manuellement plusieurs séries d'autorités fournies par le logiciel de l'Abes. Selon les résultats obtenus par le logiciel d'alignement, ces cas sont plus ou moins complexes et demandent un temps de traitement variable. L'auteur a identifié et documenté les procédures requises tout en estimant le temps que pourraient prendre ces vérifications. Avant la migration, celles-ci peuvent être faites dans un simple fichier tableur. Par contre, une fois le versement effectué dans IdRef, les corrections devront être faites manuellement dans la base de données, ce qui risque de compliquer le processus.

En multipliant les estimations de temps de traitement par le nombre de notices identifiées et en extrapolant le résultat obtenu pour les échantillons de notices à la totalité du fichier, on obtient un résultat d'environ 5'212 heures de travail pour ces vérifications.

> Ramené à une équipe de 5 personnes à plein temps cela représenterait au bas mot 26 (!) semaines de travail.

Il est évident que le temps et les ressources manquent à toutes les bibliothèques du réseau, actuellement aux prises avec la préparation d'une migration d'envergure. Néanmoins, la richesse du catalogue d'autorités de {{ smallcaps "rero" }} mérite qu'on ne laisse pas cet élément de côté, comme le constate d'Etienne Attinger dans son travail. C'est pourquoi les travaux concrets de vérification ont d'ores et déjà commencé dans les bibliothèques de {{ smallcaps "rero" }} afin que le plus d'autorités possibles soient alignées avec IdRef avant les migrations.

__Référence :__ ATTINGER, Etienne, 2020. _Étude, éléments de réalisation et évaluation de l’intégration des autorités RERO dans le référentiel francophone IdRef_. Genève : Haute école de gestion de Genève. Travail de Bachelor.

[1]: https://slsp.ch/
[2]: https://www.idref.fr/
[3]: http://www.abes.fr/Autorites-et-referentiels/IdRef-Identifiants-et-Referentiels
[4]: https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd_node.html
[5]: https://viaf.org/