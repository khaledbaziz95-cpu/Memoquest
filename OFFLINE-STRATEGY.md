# Stratégie hors ligne MemoQuest Android

## Niveau intégré dans cette version

- Si Internet est disponible : l'app charge https://khaledbaziz.online/.
- Si Internet n'est pas disponible : l'app tente de charger la version en cache.
- Si aucun cache n'existe encore : l'app affiche une page hors ligne locale.
- Le stockage local du jeu reste dans la WebView Android : localStorage / DOM storage.

## Pour un offline 100% complet dès installation

Il faudra une étape supplémentaire :

1. Exporter les données du jeu en JSON complet.
2. Emballer les cartes/images/audio/quiz dans `app/src/main/assets/memoquest-offline/`.
3. Créer un `index.html` local autonome avec React/JS et les données embarquées.
4. Lancer localement ce bundle si aucun réseau n'est disponible.
5. Synchroniser scores/pièces/progression avec WordPress quand Internet revient.

Cette version est prête comme base professionnelle Android WebView. Elle évite le simple raccourci Chrome, mais elle ne remplace pas encore une application native complète offline-first.
