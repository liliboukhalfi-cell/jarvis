# /commit

> Commande pour sauvegarder l'état actuel du workspace dans Git.

---

## Mission

Quand je lance `/commit`, exécute cette séquence :

### Étape 1 : Vérifier l'état du dépôt

Lance `git status` pour voir les fichiers modifiés.
Lance `git diff` pour voir le détail des changements.

Si aucun changement détecté, dis-le moi simplement et arrête là.

### Étape 2 : Proposer un message de commit

En regardant les fichiers modifiés, propose un message de commit clair en français.

Format du message :
- Une ligne courte qui résume ce qui a changé (max 60 caractères)
- Exemples : "Mise à jour du contexte", "Ajout de clefs API", "Nouvelle session - objectifs mis à jour"

Présente le message proposé et demande si je veux le modifier ou valider.

### Étape 3 : Commiter

Une fois validé, exécute dans l'ordre :
1. `git add .` (en excluant .secrets/ grâce au .gitignore)
2. `git commit -m "[message validé]"`

Confirme le résultat avec le hash court du commit.

---

## Règles importantes

- Ne jamais inclure le dossier `.secrets/` dans le commit (il est dans .gitignore)
- Toujours proposer le message avant de commiter, ne pas le choisir seul
- Si le .gitignore n'existe pas, signaler le risque avant de faire `git add .`
- Messages de commit en français
