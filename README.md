# Mein Wortschatz

Vokabel-Trainer Deutsch → Russisch: Karteikarten mit Artikel, Plural und Beispielsatz, Lernmodus mit 15 Wörtern pro Runde.

- Läuft komplett im Browser als statische Seite (GitHub Pages).
- `words.json` ist der Startwortschatz (270 Wörter), der beim ersten Öffnen geladen wird.
- Ohne Anmeldung liegen Wörter und Lernfortschritt im `localStorage` des Browsers.
- Mit „Войти через Google“ werden sie in Firebase Firestore (`users/{uid}/words`) gespeichert und sind in allen Browsern gleich. Beim ersten Anmelden wird der Wortschatz aus dem aktuellen Browser hochgeladen. Zugangsdaten stehen in `firebase-config.js`, die Sicherheitsregeln in `firestore.rules`. Ist `firebase-config.js` leer, läuft die App nur lokal.
- Über „Все слова → Резервная копия“ lässt sich alles als JSON sichern und wieder laden.
- Auto-Übersetzung beim Hinzufügen: de.wiktionary.org (Artikel, Plural, Übersetzung, Beispiel), Ersatz: MyMemory.
