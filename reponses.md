
# Questions

## Partie 3

### 1. l’identifiant court du premier commit
e8272a5

### 2. le commit correspondant à l’ajout de la page Contact
d8101ab

### 3. le nombre actuel de commits
6

### 4. la commande utilisée pour afficher l’historique sous forme graphique
git log --oneline --graph --all

### Examinez précisément l’un des commits correspondant à la fonctionnalité Contact et indiquez dans reponses.md la commande utilisée. 
git show d8101ab

## Partie 5

### Mission 8
j'ai utilisé
```git reset HEAD~1``` mais ```git reset --soft HEAD~1``` aurait aussi fonctionné mais mes modifications seraient resté dans le zone de staging

### Mission 9
J'ai utilisé ```git revert 66d4e81``` cela permet de faire un nouveau commit pour supprimer les anciennes modifications, alors que ```git reset``` supprime juste le commit mais ne réecrit pas l'historique

## Partie 7

### Mission 11
J'ai utilisé ```git cherry-pick 845a6f2``` la commande ```git merge``` n'aurait pas fais le resultat souhaité car sur ```main``` j'aurai récupéré tous les commits de la branch ```tets/tests```

## Partie 8

### Mission 12
Correspondances de la version ```1.0.0```
- 1er chiffre: Version majeur (1 à 2 fois par an)
- 2eme chiffre: Ajout d'une nouvelle fonctionnalité
- 3eme chiffre: Correction d'un bug mineur (hotfix)

La version suivant sera dans les cas suivants:
- une correction de bug mineur: ```1.0.1```
- une nouvelle fonctionnalité compatible: ```1.1.0```
- une refonte majeure incompatible: ```2.0.0```

## Questions final

### 1. Quelle différence existe-t-il entre la zone de travail, la zone de staging et l’historique ? 
La zone de travail comporte les changements que l'on est actuellement entrain de faire, la staging c'est la zone pour préparer une futur commit (tous ce qui est dedans sera commité), l'historique correspond à l'ensemble des commits qui compose la branch courante

### 2. Pourquoi est-il préférable de réaliser une fonctionnalité sur une branche dédiée ?

Cela permet de séparer la travail pour avoir une référence de l'état de comment était le repo avant de faire les modifications. Cela permet également dans une équipe de pouvoir faire des MR/PR pour faire des review de code

### 3. Quelle différence fondamentale existe-t-il entre les deux méthodes d’annulation utilisées dans les missions 8 et 9 ? 
```git reset``` retire un commit de l'historique sans le réecrire, tandis que ```git revert``` permet de créer un nouveau commit pour supprimer les modifications d'un ancien commit

### 4. Dans quelle situation est-il utile de mettre temporairement ses modifications de côté ? 
Si on est entrain de developper une nouvelle feature, mais que l'on doit rapidement faire une autre modification mais que l'on ne veux pas commit le code actuelle

### 5. Pourquoi la récupération d’un commit précis peut-elle être préférable à la fusion complète d’une branche ?

Cela peut être utile dans le cas ou nous ne voulons pas récuprer l'ensemble des modifications qui ont été effectué

### 6. À quoi sert HEAD ? 
Cela représente le commit ou nous sommes actuellement placé

### 7. Que représente HEAD~2 ? 
Cela signifie l'antépénultième commit

### 8. À quoi sert un tag Git ? 
Cela sert à marquer un commit pour indiquer des informations supplémentaire sur ce dernier (Ex: n° de version)

### 9. Pourquoi des commits petits et précis facilitent-ils la maintenance d’un projet ? 

Permet d'être review plus facilement par une équipe, peut permettre d'identifié quelle commit à introduit un bug dans un projet, ce dernier cas peut être fais facilement avec ```git bisect```

### 10. Pourquoi certains fichiers ne doivent-ils pas être versionnés ? 
Car ils peuvent soient être trop volumineux comme par exemple des modules, soit unique a note env local comme des logs, ou alors contenir des information confidentiel comme les .env