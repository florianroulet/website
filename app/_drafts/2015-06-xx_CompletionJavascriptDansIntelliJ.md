---
layout: post
title: Améliorer la completion JavaScript d'IntelliJ IDEA
author: Cedric
cover: banner-intellij
tags: [IntelliJ, JavaScript]
---


# IntelliJ IDEA
Tout le monde sait que nous adorons utiliser IntelliJ IDEA pour développer. 
Peu importe le langage IntelliJ est vraiment un excellent IDE qui nous permet d'être efficace quasiment instantanément.

Par contre, quand on arrive dans le monde du JavaScript on peut avoir quelques soucis pour être 
dans un environnement suffisamment typé où l'on sait ce qu'on va faire sans se poser trop de questions.

## JavaScript dans IntelliJ
Par défaut, IntelliJ est déjà suffisament malin pour scanner les fichiers du workspace 
et trouver de la complétion en automatique (ainsi que la JSDoc).

Cependant, ce mécanisme ne marche pas à tous les coups : 
 
 * vous utilisez des versions sur des CDN
 * vous avez des versions minifiées dans votre workspace
 * vous utilisez des outils qui impliquent certains framework (karma / jasmine / mocha...)
 
## Faire comprendre le JavaScript à IntelliJ
Pour réussir à obtenir une completion correcte vous avez plusieurs solutions :
 * pour les CDN, vous pouvez demander à IntelliJ de récupérer la ressource (il ne la mettra pas dans votre projet pour autant)
 * pour les versions minifiées, vous pouvez ajouter manuellement les bibliothèques dans la fenêtre de paramètres
 
## LA mega astuce
IntelliJ est capable de comprendre le TypeScript, et des gens ont eu la bonne idée de regrouper des définitions TypeScript pour
la plupart des librairies les plus utilisées dans un dépôt Github : [DefinitelyTyped](http://www.definitelytyped.org).
Dans la fenêtre de création de librairie JavaScript, dans la partie qui permet le téléchargement d'une librairie, 
sélectionnez la source "TypeScript Community Stubs", vous verrez qu'il y a beaucoup des librairies que vous utilisez au quotidien.

Avec ceci, vous aurez une completion efficace, avec le typage offert par TypeScript (dans la mesure du possible), 
ainsi qu'une documentation précise (pour la plupart des librairies).