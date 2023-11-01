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
## Aufgabe 3
  pytest test_app.py -> führt Pytest aus um die Testfälle in der test_app.py Datei durchzuführen.  
  --doctest-modules -> Damit führt Pytest Doctests aus.   
  --junitxml=junit/test-results.xml -> Die Testergebnisse werden im Unit XML-Format gespeichert.  
  --cov=com ->  Die Code-Coverage-Berechnung mit pytest-cov wird aktiviert und "com" ist das Verzeichnis in dem die Code-Coverage Berichte erstellt werden.  
  --cov-report=xml -> Die Code-Coverage Berichte werden im XML-Format erstellt.  
  Quelle: https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python
## Aufgabe 4  
  Der Link: https://tagebbuch.azurewebsites.net/
  Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen:
  Ich habe mich dazu entschieden eine Azure Key Vault-Instanz zu erstellen um das Passwort zu speichern. Dazu muss man zuerst in Azure nach "Key Vault" suchen und da kann man eine neue Instanz erstellen. Dort 
  habe ich folgendes ausgefüllt:  
![image](https://github.com/NinaWoesten/WoestenNinaLB-324/assets/105288781/4027971b-0916-46d4-93d2-922df9ad2815)  
  Nach einer kurzen Wartezeit sollte die Instanz erstellt sein und man kann nun ein "Secret" zur Instanz hinzufügen. Ich musste mir dafür noch die Berechtigung unter "Access control (IAM)" zuteilen. Dazu habe      ich mir einfach die Rolle vom Key Vault Administrator gegeben. Um ein "Secret" zu erstellen muss man nur den Namen eingeben also in dem Fall "PASSWORD" und das Passwort selber sprich "hallihallo".


