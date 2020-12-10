# git Commit

la commande 'git commit' crée un 'commit', permet de faire un instantané de votre 
référentiel. Ces commits sont des instantanés de l'ensemble de 
votre référentiel à des moments spécifiques. Il est recommandé de faire 
de nouveaux commits souvent, basés sur des unités logiques de 
changement. Au fil du temps, les commits devraient raconter 
l'histoire de votre référentiel et comment 
il est devenu tel qu'il est actuellement. Les validations 
incluent de nombreuses métadonnées en plus du contenu et du 
message, comme l'auteur, l'horodatage, etc.

Exemple:
    
    git commit -m " mettre à jour le README.md avec un lien vers le guide de contribution "

### Utilisations et options courantes pour Git Commit`

`git commit -m "votre message"` Cela démarre le processus de validation et 
vous permet d'inclure le message de validation en même temps.

`git commit -am "votre message"` En plus d'inclure le message de validation, 
cette option vous permet d'ignorer la phase de préparation. L'ajout de `-a` 
mettra automatiquement en scène tous les fichiers déjà suivis par Git 
(modifications apportées aux fichiers que vous avez déjà validés).

`git commit --amend` : Remplace le commit le plus récent par un nouveau commit.

> pour en savoir plus : https://github.com/git-guides/git-commit



sources :
> https://gist.github.com/aquelito/8596717
