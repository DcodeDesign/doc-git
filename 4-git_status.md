# git status 

```git status``` affiche l'état actuel de votre répertoire de travail et de 
votre zone de préparation Git.

La git statuscommande ne renvoie que des informations, elle ne modifiera pas les 
validations ou les changements dans votre référentiel local.

Une caractéristique utile de git statusest qu'il fournira des informations utiles 
en fonction de votre situation actuelle. En général, vous pouvez compter sur lui 
pour vous dire:

- Où HEAD pointe, qu'il s'agisse d'une branche ou d'un commit (c'est là que vous êtes 
"extrait")
- Si vous avez des fichiers modifiés dans votre répertoire actuel qui n'ont pas encore été validés
- Si les fichiers modifiés sont mis en place ou non
- Si votre succursale locale actuelle est liée à une succursale distante, alors ``git status`` vous 
dira si votre succursale locale est en retard ou en avance par des commits
Pendant les conflits de fusion, git statusvous indiquera également exactement quels fichiers sont 
à l'origine du conflit.

### Utilisations et options courantes pour git status

- ``git status``: Le plus souvent utilisé dans sa forme par défaut, cela montre une bonne base d'informations
- `git status -s``: Donner une sortie au format court
- ``git status -v``: Affiche des détails plus détaillés, y compris les modifications textuelles de tous les fichiers non validés

sources:
 >https://github.com/git-guides/git-status
