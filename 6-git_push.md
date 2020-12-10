## git push 

`git push` télécharge tous les commits de branche locale dans la branche 
distante correspondante.

`git push` met à jour la branche distante avec des validations locales. 
C'est l'une des quatre commandes de Git qui déclenche une interaction 
avec le référentiel distant. Vous pouvez également penser `git push`
à mettre à jour ou à publier .

Par défaut, `git push` met à jour uniquement la branche correspondante sur 
la télécommande. Ainsi, si vous êtes extrait dans la master branche lors 
de l'exécution git push, seule la master branche sera mise à jour. 
C'est toujours une bonne idée d'utiliser `git status` pour voir sur quelle 
branche vous vous trouvez avant de pousser vers la télécommande.

### Utilisations et options courantes pour git push

- `git push -f`: Forcer un push qui serait autrement bloqué, généralement parce qu'il supprimera ou écrasera les commits existants (à utiliser avec prudence!)
- `git push -u origin [branch]`: Utile lors de la création d'une nouvelle branche, cela crée une branche de suivi en amont avec une relation durable avec votre branche locale
- `git push --all`: Pousser toutes les branches
- `git push --tags`: Publier des balises qui ne sont pas encore dans le référentiel distant

sources:
>https://github.com/git-guides/git-push
