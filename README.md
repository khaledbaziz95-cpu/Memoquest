# MemoQuest Android APK Project

Projet Android natif pour ouvrir MemoQuest comme une vraie application Android indépendante de Chrome.

Site configuré : https://khaledbaziz.online/
Package : `com.memoquest.game`

## Ce que contient l'application

- WebView Android plein écran.
- Icône MemoQuest.
- Chargement direct de `https://khaledbaziz.online/`.
- Cache WebView + support DOM storage/localStorage.
- Tentative de chargement depuis le cache en mode hors ligne.
- Page offline locale propre si le cache n'est pas encore disponible.
- Ouverture externe sécurisée pour PayPal / Google / Facebook.
- Deep link de base : `memoquest://app`.

## Build APK

1. Installe Android Studio.
2. Ouvre ce dossier comme projet Android.
3. Attends la synchronisation Gradle.
4. Clique **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. L'APK debug sera généré dans :

```text
app/build/outputs/apk/debug/app-debug.apk
```

Pour une version Play Store ou partage officiel, crée une clé de signature puis utilise **Generate Signed Bundle / APK**.

## Important

Cette app est un vrai APK Android, indépendant de l'icône Chrome. Elle charge ton site WordPress MemoQuest et utilise le cache local quand c'est possible.
Pour un mode hors ligne 100% complet dès la première installation, il faudra embarquer une version statique complète du jeu et de toutes les cartes/quiz dans les assets Android, ou transformer MemoQuest en application Capacitor avec synchronisation locale.
