# Teammeeting 21.09.2022 20:45-23:00

## Todos

1. Einarbeitung/Tutorials
   * Sprachen & Frameworks
     * Flutter (essentiell)
     * Swift & Kotlin (zweitrangig)
   * CI/CD Pipeline für Flutter Projekte
2. Demo Projekt aufsetzen
   * Git Repository
   * Flutter Demo Projekt (nur 1-2 "Dummy-Features")
   * Tests für Flutter Demo Projekt
     * Unit
     * UI
3. Integration des Flutter Demo Projekts in die CI/CD Pipeline
   * automatisierte Tests beim Pushen auf den "release" Git Branch
   * Binary Files werden gebaut
4. Echte Features (kommt dann ...)

## Über uns

* [ ] Wenig bis keine Erfahrung in App-Dev/Flutter/Dart
  * [ ] Tutorials durcharbeiten
* [x] Gute Erfahrung mit Scrum, CI/CD
* [x] Studiengang: Software Engineering, 3/4 von Informatik gewechselt
* [x] Alle haben bestandenes Softwaregrundprojekt
* [x] Plattformen: Windows, Linux, Mac OS
* [ ] Bekannte IDEs/Editoren: IntelliJ, VSCode, Notepad++, Visual Studio, Android Studio
  * [ ] alle VSCode als Haupteditor verwenden
  * [ ] Xcode & Android Studio nur für Plattform spezifische Probleme verwenden (sofern unbedingt notwendig)

## Offene Fragen

* [ ] Genauere Definition des Backends, Welche Sprache?, Server oder Lokal?
  * [ ] Erstmal noch zweitrangig (weiteres beim nächsten Treffen)
    * [ ] Docker (Compose)
      * [ ] Datenbank (PostgreSQL, MariaDB)
      * [ ] Framework (NodeJS, Laravel, Parse)
* [x] Was sind EMA Fragebögen? Definition und Beispiele
  * ist erstmal zweitrangig
  * Ecological Momentary Assessment
    * ganz grob zusammengefasst geht es um Fragebögen
    * an welche mit Notifications erinnert wird
    * in natürlichen Umgebung des Benutzers (im Alltag)
* [x] Wollen Sie an der Zeiterfassung teilhaben? Vorgaben?
  * Tabelle (Chronologisch sortiert)
    * Datum
    * Name
    * Zeit in h (auf 15 min genau)
    * Tätigkeitsbeschreibung
    * Ticket(s)
* [x] Wie wird unsere library getestet? Gibt es Test-Geräte/-Studien-Apps?
  * CI/CD Pipeline mit Demo App aufsetzen
  * Wichtig
    * automatisierte Emulator Tests
    * und Unit Tests
  * Zweitrangig
    * Integration Tests

## Organisatorisches

### Treffen

* [x] Ja, wöchentlich oder alle 2 Wochen (intern), evlt. auch mehrmals die Woche
* [x] Mit Betreuern nach Bedarf (je nach dem wie stark involviert die sein wollen)
  * wir wollen alle zwei Wochen Freitags ein kurzes Treffen zum Zwischenstand (~30 min)
    * insgesamt max. 20 min berichten was ihr (jeweils) gemacht habt
      * dazu zählt auch "ich habe das Tutorial X durchgearbeitet", "... die Doku Y gelesen" oder "...mich um Feature/Bug Z gekümmert"
    * dann können wir das Ganze bei Bedarf besprechen bzw. weiteres planen (~10 min)
* [x] Mit Betreuern vor Ort, Intern Online/vor Ort (von Fall zu Fall)
  * online (im Normalfall)
* [x] 2 Wochen Sprints (Planning, Reviewing)
  * passt zum Turnus der Onlinetreffen
  * Betreuertermine sind nicht die Sprintreviews
  * die Sprintreviews führt ihr unter euch durch und liefert uns dann nur die Ergebnisse

### Rollen

* [ ] Rollen: unklar (je nach Projekt, am besten nach Komponenten)
* [ ] Scrum-Master, DevOps Rollen
* [ ] Kontroll-Instanzen Docs, DevOps, Formatierung, GitLab-Pflege, Projekt-Pflege, ...
* [ ] Protokollant: Felix

=> organisiert euch wie ihr wollt, bedenkt aber, dass beim Rotieren der Rollen ggf. mehr Zeit zum Einarbeiten nötig ist (und Verzögerungen druch Rollenübergaben usw.), bitte bis 14.10.2022 intern klären

## Meilensteine

besprechen wir am 14.10.2022

1. **Anfang/Mitte November:** [ ] Anforderungen festlegen 
2. **November-Dezember:** [ ] Entwurf
3. **Februar-März:** [ ] MVP (minimal viable product)
4. **März:** [ ] Fertigstellung, größeres Testen
5. **April:** [ ] Präsentation

* [ ] Benötigt genauere Projekt Beschreibung (TBA)
* [ ] Zwischenvorstellung 25.1.2023
* [ ] Abgabe 26.4.2023

## Workflow

* [ ] Rebase vs Merge inkl. Squashen (muss noch entschieden werden, jeder selber Gedanken machen)
  * kein Squashen
* [ ] Gitflow workflow (1x main, 1x develop, beliebig feature branches)
* [ ] Sprints = Milestones = Releases in GitLab
* [x] Prefixes für branches (fix/, feature/, refactor/, ci/, experimental/)
* [ ] https://www.conventionalcommits.org/en/v1.0.0/
* [x] Branch protection
* [x] Merge approval
* [x] Scrum stages:
  * [x] To Do
  * [x] In Process
  * [x] Review
  * [x] To Be Merged
  * [x] Done

## Pipeline

* [x] Nur merge auf main/develop, wenn pipeline erfolgreich ist
* [x] Stages:
  * [x] Linting/Code Formatting
  * [x] Testing
  * [x] Build iOS, Android
    * [ ] Deploy? iOS, Android => reden wir noch
  * [x] Dokumentation
* [x] Bei Drafts keine Pipeline ausführen (bzw. minimal)

## Tools

* [x] Nutzen von .editorconfig https://editorconfig.org/ (einheitliche Editor Einstellungen)
* [x] VSCode
* [ ] IntelliJ => nein
* [x] AndroidStudio
