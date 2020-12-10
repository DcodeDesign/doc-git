# Guide Git 

### Create a new repository on the command line
    
    echo "# name-projet" >> README.md 
    
crée un fichier readme.md avec le contenu # name-projet
    
    > git init
    > git add README.md
    > git add -A
    > git commit -m "first commit"
    > git remote add origin git@github.com:Thomasgravy/signatures-side.git
    > git push -u origin master
    > git push -u origin master --force

### create projet
    > mkdir firstProjet
    > cd firstProjet
    > git init
    > git help config (q -> exit)
    > git config --global user.email "gravythomas@gmail.com"
    > git config --global user.name "Dcode-design"
    > git config --global color.ui true
    > git config --list

### Create files
    > touch readme.md
    > dd if=/dev/zero of=image.jpg  bs=1m  count=240
    > rm image.jpg
    > dd if=/dev/zero of=texte.txt  bs=1m  count=240
    > touch index.html
    > touch home.html
    > touch lol.html

### Create commit
staging (untraked files) => zone de transit

    > git status
    > git add readme.md (permet de traquer un fichier) 
    > git add docs.txt
    > git add "*.html"
    > git add "*.txt"
    > git add --all

### Commit
    > git commit
    
```vi``` ouvre le commit dans terminal 

```i``` passe en mode insertion

```(esc) :wq ```

    > git commit -m "Mon quatrième commit"
    > git commit -a -m "ciquième commit" 
git add + stage all file + commit


### Create gitignore
    > touch .gitignore

### Log commit
    > git log
    > git log -2

    > git help log

    > git log -p readme.md
    > git log -n 1 -p readme.md

    > git log --oneline -p readme.md

    > git diff 
    > git diff <fichier>
    
    > git restore <file>
    
    > git diff <commit> 
    
comparera l'état actuel au commit <commit>

    > git diff <commit>...<commit> 

#### Revenir en arrière
    > git log --oneline -p readme.md
    > git checkout 6912b29
    
sha1 du commit dont ou l'on voudrait revenir

    > git checkout master 
attention si des modif on eu lieu cela affichera un messahe pour demander de faire un commit
cette méthode ne permet pas de revenir a une version précédent mais de voir ce qui à été fait

pour reprendre une version du code précédent : 

    > git checkout 6bc30da readme.md 
    
reprend les modification du fichier au commit 6bc30da

    > git revert 6912b29 
defait ce qui à été fait lors de ce commit mais ne modifi pas l'historique
    
    > git revert e020961 
annule le revert 

supprime et revient à une version précédente
    > git reset HEAD index.html
    
enlève le staging sur le document
    
    > git reset 
    
enlève tous les staging 
    
    > git reset --hard 
    
efface toutes les modification et revient au commit précédent
    
    > git reset e020961 
    
revient au commit mentionner mais garde les dernières modification  (modifie l'historique !!!)
    
    > git reset HEAD^ --soft##### revient à la version précédente, nombre de ^ = à la version en gardant les modification

### les Branches
    > git branch newBranch
    > git checkout newBranch
    > git checkout master
    > git branch -d newBranch 
    
supprime la branche

    > git merge newBranch
    > git merge --no-ff newBranch 

### rebase & merge
Dans Git, il y a deux façons d’intégrer les modifications d’une branche 
dans une autre : en fusionnant (merge) et en rebasant (rebase).
    
    > git rebase master serveur 

Cette commande rejoue les modifications de serveur sur le sommet de la branche master

### Fetch & pull

##### Manipulation de l'historique
    > git commit --amend 

modifier un commit précédent car oubli

    > git rebase merge newBranch 

permet de rapatrier tous les commits d'une branche sur une autre 
attention de ce mettre sur la branche sur laquelle on veut rapatrier les commit
    
    > git branch new
    > git checkout new
    > git rebase -i master 

**Commands:**
- p, pick = use commit
- r, reword = utilisez commit, mais modifiez le message de commit
- e, edit = use commit, arrêter pour modifier
- s, squash = use commit, fusionner avec le commit précédent
- f, fixup = like "squash", ignorer le message du journal de ce commit
- x, exec = exécuter la commande (le reste de la ligne) en utilisant le shell
- d, drop = remove commit

```
git rebase -i HEAD^^^ 
```

fusionne les 3 dernier commit

### Remisage (stach) 
##### stock en local sans commit
    > git stash 

stock les modif en mémoire

    > git stash list
    > git stash apply 
    
remet les modifications stocker en mémoire

    > git stash save nom_du_stach
    > git stash drop

    > git stash show stash@{1}
    > git stash show stash@{1} -p
    > git stash apply stash@{1}
    > git stash apply stash@{1}
    > git stash drop stash@{1}

    > git stach pop = git stash apply + git stash drop

    > git stash branch 'demo'
     
crée une branche avec les donnée du stach

    > git stash -u 

rajout des fichier dasn le stash

### Remote 
    > git init --bare 
dossier qui resevra les dépots - centralise les dépots

    > git remote add origin /Users/thomasgrav/Desktop/WORKSPACE/WORKSPACE-GIT/depot-remote (ssh://)

dépots local

    > git remote -v
    > git remote rename origin lol

    > git branch -r 
    
voir les Branches

    > git push origin test
    
    > git branch -d new 
    
supprime une branche 

    > git branch -D new 
    
supprime une branche 

    > git push origin --delete test 

supprime la branche sur le dépots

    > git clone /Users/thomasgrav/Desktop/WORKSPACE/WORKSPACE-GIT/depot-remote
    > git clone /Users/thomasgrav/Desktop/WORKSPACE/WORKSPACE-GIT/depot-remote newProjet 

create folder newProjet

    > git pull origin master
    > git pull --rebase origin master

    > git fetch <remote>

##### fork & request
    
    > ...

## Resources
##### Hook
    https://developer.github.com/webhooks/# GIT-initProjet
##### git install
    https://git-scm.com/downloads

##### commandes
    https://git-scm.com/docs/git#_git_commands

##### path GIt executable 
    /usr/local/bin/git

##### Create Key ssh
    > cd (alt + n) ~/.ssh (on mac)
    > ssh-keygen -t rsa -C "gravythomas@gmail.com"
        id_rsa
        id_rsa.pub

##### doc github 
    https://gist.github.com/aquelito/8596717

##### ungit
    > sudo -H npm install -g ungit
    > ungit

##### gitgraphjs.com
    permet de modéliser un graph github

##### vi
    :wq
