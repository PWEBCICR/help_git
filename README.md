# help_git
Quelques petits conseils sur GitHub

## Les bases

On a un repo, ça correspond à un dossier de travail. Dans celui-ci on aura forcément un readme.md, ça peut être bien de le compléter pour savoir où on en est et bien détailler le bordel (peut être qu'on va devoir le faire en anglais, ça dépendra du cahier des charges (si projet en Anglais ou non)).

Pour travailler sur ce repo, il faut le cloner sur ta machine. `git clone lien_de_mon_repo` (on peut faire un clonage http ou un clonage ssh).
On fait nos modifs sur le repo (si ce sont des nouveaux fichiers, on les ajoutes (`git add mon fichier`)). Quand on les modifs sont finies, on fait un `commit` (ON PEUT FAIRE UN MAX DE COMMIT). Il ne faut pas attendre d'avoir fait 5h de code pour commit. Github c'est un gestionnaire de version, c'est donc grave pratique. Si une modif plante on peut toujours ('fin normalement) revenir à une version précédente. 

- Synchroniser avec le repo github : `git pull`
- Synchroniser avec une certaine branche : `git checkout ma_branche`
- Ajouter du contenu (genre un nouveau fichié) : `git add nom_fichier` (meme principe avec `delete` (je crois ^^))
- Enregister mes modifications : `git commit -m "Écrire un message correspondant aux modifs" .` (le point c'est pour dire qu'on bosse dans le dossier courrant, tu peux bosser sur un certain dossier/fichier)
- Envoyer mon dernier commit sur le serveur `git push`

## Notions de branches

L'idée avec les branches c'est que tu créés une copie d'une autre branche. Tu travailles sur la nouvelle branche (qui est donc une copie) et quand tout fonctionne, tu fais une `Pull request` pour fusionner tes modifications avec la branche principale. On va exploiter ce principe très pratique puisqu'il permet de toujours avoir une version fonctionnelle dans la branche principale !

Une `pull request` c'est donc un peu risqué puisqu'une fois dans la branche principale, on considère que c'est une version fonctionnelle ! C'est pourquoi je vais paramètrer un système de reviewers. Dans l'idée, il faut qu'un certains nombre de personne approuve la PR (`pull request`) pour que celle-ci se fasse. 

## Notion d'issue

Travailler avec des issues c'est super pratique. L'idée c'est de lever un ticket pour soutenir une modification du code. Ça peut être fait pour un bug, une question, des nouvelles features, … Un peu tout en fait.

Lorsqu'on lève une issue, on peut lui mettre un petit label (ça permet de voir la gravité de l'issue), on peut l'assigner à une personne (ça permet de gérer le projet c'est beau) et on peut la linker à un projet.

## Les projects boards

C'est un joli outils github qui permet d'avoir une bord de gestion de projet. L'interface graphique est plutôt cool et on voit où on en est et ce qu'il nous reste à faire, c'est vraiment pas mal. Il y a des sections TODO / in progress / done / ……… Ce qui est encore plus joli c'est que l'outil peut être automatisé. 
Je m'explique : 
- On lève une issue "BUG à l'affichage"/on la lie au projet et tout la tralala --> Sur la project board l'issue est ajoutée à TODO
- On assigne qqn à la correction du bug --> Une nouvelle branche est crée &&  Sur la project board l'issue passe de TODO à IN PROGRESS
- On ferme l'issue et on PR la nouvelle branche -->  Sur la project board l'issue est ajoutée à DONE

On peut aller plus loin en gérant les reviews des PR c'est cool aussi !
