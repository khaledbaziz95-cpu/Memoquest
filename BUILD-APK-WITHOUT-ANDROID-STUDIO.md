# Générer l'APK MemoQuest sans Android Studio

Ce projet contient un workflow GitHub Actions qui compile automatiquement un APK installable.

## Étapes

1. Crée un dépôt GitHub vide.
2. Envoie tous les fichiers de ce dossier dans le dépôt.
3. Va dans l'onglet **Actions**.
4. Ouvre **Build MemoQuest APK**.
5. Clique sur **Run workflow**.
6. Attends la compilation.
7. Ouvre le run terminé et télécharge l'artifact **MemoQuest-installable-debug-apk**.
8. Dézippe l'artifact : tu obtiens `app-debug.apk`.
9. Envoie ce fichier sur ton téléphone et installe-le.

## Important

- C'est un vrai APK Android installable.
- Il est signé en debug, donc Android peut afficher un avertissement lors de l'installation.
- Pour une version Play Store, il faudra une signature release officielle.
