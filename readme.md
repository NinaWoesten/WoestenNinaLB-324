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
  Beispiel:  
  ![Screenshot 2023-11-03 124853](https://github.com/NinaWoesten/WoestenNinaLB-324/assets/105288781/2cec6f08-2609-417f-94a9-c4246d715bb5)

## Aufgabe 4  
  Der Link: https://tagebbuch.azurewebsites.net/  
  Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen:  
  Ich habe mich dazu entschieden eine Azure Key Vault-Instanz zu erstellen um das Passwort zu speichern.  
  ### Schritt 1: Azure Key Vault-Instanz erstellen
  Dazu muss man in Azure nach "Key Vault" suchen und dieses dan auswählen. Auf der nun erschienen Seite kann man mit "create" eine neue Instanz erstellen. Dazu muss man nur einen Namen eingeben, alles andere 
  kann so belassen werden: 
  ![image](https://github.com/NinaWoesten/WoestenNinaLB-324/assets/105288781/4027971b-0916-46d4-93d2-922df9ad2815)  
  Sobald die Instanz erstellt wurde kann man zum nächsten Schritt übergehen:
  
  ### Schritt 2: Konfiguration der Zugriffsberechtigungen
  Bevor ich ein Secret erstellen konnte musste ich mir noch die entsprechende Berechtigungen geben. Dazu bin ich auf die Registerkarte "Access control (IAM)" gegangen und habe mir die Rolle "Key Vault- 
  Administrator" zugewiesen. Nun kann man ein "Secret" erstellen
  ### Schritt 3: Secrets hinzufügen
  Dazu muss man in der eben erstellten Instanz auf "Secrets" gehen und dort eine neues Secret erstellen. Jetzt muss man dem Geheimnis einen Namen geben (PASSWORD) und dann den Wert des Passworts (hallihallo) 
  definieren. Und auf "Create" klicken. 

  ### Schritt 4: Secret-ID 
  Nachdem das Secret erfolgreich erstellt wurde, muss man sich nur noch die Secret-ID aufschreiben, um darauf in der Anwendung zugreifen zu können.



