## Pousser ses modifications sur un repos distant

1. `git commit -am "message"`  or `git stach` permet de sauvegarder les dernières modifications
2. `git push` pousse les fichiers sur le repo distant

## Récupérer ses modifications d'un repos distant
***S'assurer que ces modifications soient commiter.***
1. `git commit -am "message"` // commiter tous les changements de la branche 
2. `git fetch --prune` permet de récupérer l'historique des 
modifications de la branche master en local et de résoudre les conflits si il y en a.
3. `git pull -r` récupérez les modifications distantes avec l'indicateur --rebase , 
vos modifications locales sont réappliquées en plus des modifications distantes.

## Création d'une nouvelle branche
    
1. `git add .` permet de s'assurer de tracker tous les fichiers
2. `git commit -am "message"`  or `git stach` permet de sauvegarder les dernières modifications
3. `git branch [branch_name]`  crée un nouvelle branche en local
4. `git checkout [branch_name]`
6. `git add .` track les changements à travers tout le référenciel local 
7. `git commit -m "init commit"` permet de soumettre les mise à jour pour le pousser sur le repos distant 
8. `git push origin [branch_name] ` pousse les fichiers sur la nouvelle branche

## Pousser les modifications d'une branche vers la branche master

1. `git commit -am "message"` // commiter tous les changements de la branche 
2. `git push origin [branch xxx] ` pousse les fichiers sur la nouvelle branche
3. `git checkout master`  passer sur la branche master

***S'assurer que ça branche master local est à jour.***
4. `git fetch --prune` permet de récupérer l'historique des 
modifications de la branche master en local et de résoudre les conflits si il y en a.
5. `git pull -r` récupérez les modifications distantes avec l'indicateur --rebase , 
vos modifications locales sont réappliquées en plus des modifications distantes.

***Récuperer les modifications de la branch xxx***

6. `git fetch --prune origin [branch xxx]` permet de récupérer l'historique des 
modifications de la branche branch xxx distante et de résoudre les conflits si il y en a.
7. `git pull -r origin [branch xxx]` récupérez les modifications distantes avec l'indicateur --rebase , 
vos modifications locales sont réappliquées en plus des modifications distantes.


sources:
> https://www.datree.io/resources/git-push-force
> https://github.com/git-guides/git-commit
> https://gist.github.com/aquelito/8596717
