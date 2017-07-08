# hunter_master
Master repo with our patches on hunter, boost, opencv and gtest

Ce repo est sur la branche master, et tous ses sous-repos sont sur une branche nommée ivs :

```
git config -f .gitmodules submodule.hunter.branch ivs
git config -f .gitmodules submodule.googletest.branch ivs
git config -f .gitmodules submodule.opencv.branch ivs
git config -f .gitmodules submodule.boost_patch_warnings.branch ivs
```


Les submodules opencv et googletest sont des forks des version hunter : pour ajouter des remotes "official" pointant vers les repo officiels, faire les commandes :

```
cd opencv
git remote add official https://github.com/opencv/opencv.git
cd ..
cd googletest
git remote add official https://github.com/google/googletest.git
cd ..
```


#### Alias git pour submodules
Il est recommandé d'utiliser les alias git fournis dans GitAliases.ini (ceux qui commencent par sm-). Ils permettent de faciliter le travail avec les submodules.

Editez votre fichier ~/.gitconfig et ajoutez :

```
[include]
	path = path/to/GitAliases.ini
```
