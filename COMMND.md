# Cloner un projet

git clone [url]

# Initialiser un dépôt

git init

# Suivre des fichiers ou les ajouter à la staging area

git add fichier1 fichier2

# retrancher un fichier du staging (défaire le git add)

git reset HEAD fichier

# Voir le statut
git status

# Visualiser ce qui a été modifié mais pas encore indexé
git diff

# visualiser les différences entre un commit et l'état actuel ou un autre commit
git diff commithash [commithash2]

# idem que ci-dessus mais seulement pour les fichiers précisés
git diff commithash [commithash2] fichier1 [fichier2 …]

# Demander à git d'afficher les diff des fichiers ajouté à la staging (avec git add)
git diff --staged

# Visualiser les modifications indexées qui feront partie de la prochaine validation
git diff --staged

# Enregistrer "commiter" les modifs
git commit

# Commiter sans passer par l'éditeur de texte
git commit -m "message de commit"

# Tout comiter sans passer par add
git commit -a

# Placer un tag (lightweight)
git tag 1.2.0

# Placer un tag sur un commit antérieur
git tag 1.1.4 ffaae76

# push n'envoie pas les tags par défaut
# pour pusher les tags
git push --tags

# Voir l'historique des commits (l'option --all permet de voir l'ensemble des branches)
# il est possible d'appeler l'option --graph pour rendre ça plus visuel
# on peut préciser un fichier pour n'obtenir que les commits relatifs à ce dernier
git log [--all]

# effectuer une recherche dans les commits (-g pour toutes les branches)
git log [-g] --grep=STRING

# rechercher dans le code en incluant l'historique
# (pratique pour retrouver quelque chose qui n'existe plus dans le HEAD)
git grep 'votre recherche' $(git rev-list --all)