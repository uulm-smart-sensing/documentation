# Teammeeting 21.09.2022 20:45-23:00

## Über uns
- Wenig bis keine Erfahrung in App-Dev/Flutter/Dart
- Gute Erfahrung mit Scrum, CI/CD
- Studiengang: Software Engineering, 3/4 von Informatik gewechselt
- Alle haben bestandenes Softwaregrundprojekt
- Plattformen: Windows, Linux, Mac OS
- Bekannte IDEs/Editoren: IntelliJ, VSCode, Notepad++, Visual Studio, Android Studio

## Offene Fragen
- Genauere Definition des Backends, Welche Sprache?, Server oder Lokal?
- Was sind EMA Fragebögen? Definition und Beispiele
- Wollen Sie an der Zeiterfassung teilhaben? Vorgaben?
- Wie wird unsere library getestet? Gibt es Test-Geräte/-Studien-Apps?

## Organisatorisches
### Treffen
- Ja, wöchentlich oder alle 2 Wochen (intern), evlt. auch mehrmals die Woche
- Mit Betreuern nach Bedarf (je nach dem wie stark involviert die sein wollen)
- Mit Betreuern vor Ort, Intern Online/vor Ort (von Fall zu Fall)
- 2 Wochen Sprints (Planning, Reviewing)
### Rollen
- Rollen: unklar (je nach Projekt, am besten nach Komponenten)
- Scrum-Master, DevOps Rollen
- Kontroll-Instanzen Docs, DevOps, Formatierung, GitLab-Pflege, Projekt-Pflege, ...
- Protokollant: Felix

## Meilensteine
1. **Anfang/Mitte November:** Anforderungen festlegen 
2. **November-Dezember:** Entwurf
3. **Februar-März:** MVP (minimal viable product)
4. **März:** Fertigstellung, größeres Testen
5. **April:** Präsentation

- Benötigt genauere Projekt Beschreibung (TBA)
- Zwischenvorstellung 25.1.2023
- Abgabe 26.4.2023

## Workflow
- Rebase vs Merge inkl. Squashen (muss noch entschieden werden, jeder selber Gedanken machen)
- Gitflow workflow (1x main, 1x develop, beliebig feature branches)
- Sprints = Milestones = Releases in GitLab
- Prefixes für branches (fix/, feature/, refactor/, ci/, experimental/)
- https://www.conventionalcommits.org/en/v1.0.0/
- Branch protection
- Merge approval
- Scrum stages:
  - To Do
  - In Process
  - Review
  - To Be Merged
  - Done

## Pipeline
- Nur merge auf main/develop, wenn pipeline erfolgreich ist
- Stages:
  - Linting/Code Formatting
  - Testing
  - Build iOS, Android
    - Deploy? iOS, Android
  - Dokumentation
- Bei Drafts keine Pipeline ausführen (bzw. minimal)

## Tools
- Nutzen von .editorconfig https://editorconfig.org/ (einheitliche Editor Einstellungen)
- VSCode, IntelliJ, AndroidStudio