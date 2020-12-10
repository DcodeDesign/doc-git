# git init or push

# Démarrer un nouveau référentiel git

Il existe plusieurs manières de démarrer un nouveau référentiel git.
ici nous prendrons comme base que le repos sera créé via l'interface
d'une plateforme de versioning Git.

De manière général les plateformes tel que Github ou Gitlab vous suggère
les commandes pour initialiser le versioning de votre projet

**exemple avec Github :**

... un nouveau référentiel à partir de zero

    mkdir monProject
    cd monProject
    echo "# test-git" >> README.md 
    git init 
    git add README.md 
    git commit -m "first commit" 
    git branch -M main 
    git remote add origin https://github.com/username/monProject.git
    git push -u origin main

... pousser un référentiel existant
    git clone https://github.com/username/monProject.git
    git add [file].php
    git push -u origin [branch]
    
    
sources
> install git : https://github.com/git-guides/install-git
> git init : https://github.com/git-guides/git-init
> git clone : https://github.com/git-guides/git-clone
