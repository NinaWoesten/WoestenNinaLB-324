# LB 324

## Aufgabe 2
Erklären Sie hier, wie man `pre-commit` installiert.
### Schritt 1:
  Um "Pre-commit" auf dem lokalen Rechner zu installieren muss folgender Befehl ausgeführt werden:
  ```bash
  pip install pre-commit
```
### Schritt 2:
  Jetzt muss "pre-commit" in der lokalen Git Repository installier werden:
  ```bash
  pre-commit install
```
### Schritt 3:
  Nun kann die Kofigurationsdatei ausgeführt werden. Der folgende Befehl führt die pre-Commit-Hooks für alle Dateien in dem Repository aus. 
  ```bash
  pre-commit run --all-files
```
### Schritt 4:
  Wenn alle Hooks erfolgreich ausgeführt worden sind, kann man die Änderungen manuell comitten und pushen. 
  
## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.
