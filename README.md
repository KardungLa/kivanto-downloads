<img src="assets/kivanto-mark.png" width="72" alt="Kivanto">

# Kivanto Solo

**Deine Dateien, dein Wissen und deine Aufgaben – an einem Ort auf deinem Rechner.**

Mit Kivanto organisierst du Dokumente in Projekten, stellst deiner KI Fragen zu deinen Unterlagen und verwaltest Kontakte und Aufgaben. Der Wissensgraph macht Zusammenhänge zwischen den Inhalten sichtbar.

**[Zu den Downloads →](https://github.com/KardungLa/kivanto-downloads/releases/latest)** · [English](README.en.md)

## Was du mit Kivanto machen kannst

- **Mit deinen Dokumenten arbeiten:** Dateien hochladen oder lokale Ordner einbinden, Inhalte durchsuchen und Fragen dazu stellen.
- **Wissen verbinden:** Entitäten und Beziehungen im Wissensgraphen erkunden und als TTL, CSV, Excel oder Markdown exportieren.
- **Kontakte und Aufgaben organisieren:** Das integrierte CRM direkt oder über den Chat nutzen. Änderungen des Agents prüfst und bestätigst du im Chat.
- **Deine KI wählen:** Zum Beispiel Ollama, LM Studio, OpenAI, Mistral, OpenRouter oder einen eigenen kompatiblen Anbieter verwenden.
- **Andere KI-Assistenten anbinden:** Kivanto mit Claude Desktop, Claude Code oder Codex verbinden.

Kivanto Solo hieß bisher **Kivanto Free Local**. Ältere Downloads und bereits installierte Apps können noch den bisherigen Namen tragen.

## 1. Die passende Version herunterladen

Öffne die [Download-Seite](https://github.com/KardungLa/kivanto-downloads/releases/latest) und klappe bei der gewünschten Version **Assets** auf. Wähle die Datei für deinen Rechner:

| Dein Rechner | Passende Datei |
| --- | --- |
| Mac mit Apple-Chip, etwa M1, M2, M3 oder M4 | Dateiname enthält **`macos-arm64`**, endet auf **`.dmg`** |
| Mac mit Intel-Prozessor | Dateiname enthält **`macos-x64`**, endet auf **`.dmg`** |
| Windows-PC mit Intel- oder AMD-Prozessor, 64 Bit | Dateiname enthält **`windows-x64`** und endet auf **`-de.exe`** |
| Linux-PC mit Intel- oder AMD-Prozessor, 64 Bit | **`linux-x64`**: **`.deb`** für Ubuntu/Debian oder **`.tar.gz`** zum Entpacken |

Auf dem Mac findest du den Chip unter ** → Über diesen Mac**. Für einen englischen Windows-Installer wähle die Datei mit **`-en.exe`**. Die Anwendung selbst lässt sich auf Deutsch oder Englisch verwenden.

**Nimm den Installer für dein Betriebssystem.** Die Dateien „Source code“ und die `.jar` sind für die normale Desktop-Installation nicht erforderlich. Java und die lokale Datenbank sind im Installer enthalten.

Der Download-Link führt zur aktuellen **stabilen Version**. Ältere **Pre-release**-Versionen sind nur für Tests gedacht. Bei Paketen mit **`unsigned`** ist der Herausgeber noch nicht digital bestätigt; dein Betriebssystem kann deshalb eine Sicherheitsmeldung anzeigen. Beachte die Hinweise zur jeweiligen Version.

Wenn unter **Assets** noch keine passende Installationsdatei steht, ist für diese Plattform noch kein Download verfügbar.

## 2. Kivanto installieren

### macOS

1. Öffne die heruntergeladene `.dmg`-Datei.
2. Ziehe **Kivanto Solo** in den Ordner **Programme**.
3. Starte Kivanto aus **Programme**.

### Windows

1. Öffne die heruntergeladene `.exe`-Datei.
2. Folge dem Installationsassistenten.
3. Starte **Kivanto Solo** über das Startmenü oder die Desktop-Verknüpfung.

### Linux

**Ubuntu/Debian:** Öffne die heruntergeladene `.deb`-Datei mit der Softwareverwaltung und installiere Kivanto. Alternativ im Download-Ordner:

```sh
sudo apt install ./Kivanto-*-linux-x64-unsigned.deb
```

Starte **Kivanto Solo** danach über das Anwendungsmenü. Verwende die App mit deinem normalen Benutzerkonto.

**Portable Version:** Entpacke die `.tar.gz`-Datei in einen eigenen Ordner und starte darin `Kivanto Solo/bin/Kivanto Solo`. Java ist enthalten. Benötigt wird ein Linux-x64-Desktop mit glibc ab 2.35, X11 oder XWayland sowie `xdg-utils`. Auf Ubuntu 22.04 oder neuer sind die grundlegenden Desktop-Bibliotheken normalerweise bereits vorhanden.

Der vorgeschlagene Datenordner ist `~/.local/share/Kivanto/instance/`. Bei einem angepassten `XDG_DATA_HOME` liegt er stattdessen dort unter `Kivanto/instance/`. Die portable App und der Installer verwenden denselben Datenordner.

Beim ersten Start führt dich der Einrichtungsassistent durch die Einrichtung. Wähle die Sprache, lies und akzeptiere die Nutzungsbedingungen und bestätige den Speicherort. Die vorgeschlagenen Einstellungen kannst du zunächst übernehmen.

Anschließend öffnet sich Kivanto im Browser. Die Desktop-App läuft dabei im Hintergrund weiter.

## 3. Deine KI einrichten

Im Schritt **KI-Modell einrichten** wählst du deinen Anbieter und dein Modell. Mit **Modelle laden** rufst du die verfügbaren Modelle ab; mit **Verbindung testen** prüfst du die Verbindung.

- **Lokale KI:** Starte Ollama oder LM Studio und lade dort ein Modell. In LM Studio muss zusätzlich der lokale Server laufen.
- **Cloud-KI:** Trage den API-Schlüssel deines Anbieters ein. Ein Chat-Abonnement ersetzt diesen Schlüssel nicht; für die API-Nutzung können separate Kosten entstehen.

Du kannst diesen Schritt überspringen und später über das Kivanto-Symbol unter **KI-Modell einrichten** nachholen. Für KI-Antworten und die automatische Erkennung von Zusammenhängen brauchst du einen erreichbaren, eingerichteten KI-Anbieter.

## 4. Dein erstes Projekt anlegen

1. Öffne **Projekte → Neues Projekt** und lege ein Projekt an.
2. Lade unter **Dateien** deine Unterlagen hoch – mehrere Dateien gleichzeitig sind möglich.
3. Warte, bis Kivanto die Inhalte eingelesen hat. Den Fortschritt siehst du beim Projekt.
4. Öffne den **Chat** und stelle eine Frage, zum Beispiel: „Fasse die wichtigsten Punkte dieser Unterlagen zusammen.“

Du kannst auch einen vorhandenen Ordner hinzufügen. Als **Projektordner** arbeitet Kivanto direkt mit den Originaldateien. Als **Quelle zum Einlesen** übernimmt Kivanto Kopien; die Originale bleiben unverändert. Spätere Änderungen an einer Quelle holst du mit **Synchronisieren** ins Projekt.

Allgemeine Fragen kannst du auch ohne Dokumente stellen. Für Antworten über deine eigenen Unterlagen müssen diese zuerst eingelesen sein. Die semantische Suche benötigt zusätzlich ein eingerichtetes Embedding-Modell; dieses wird getrennt vom Chat-Modell konfiguriert.

## Kivanto im Alltag

Das Kivanto-Symbol findest du auf dem Mac in der Menüleiste und auf Windows im Infobereich der Taskleiste, gegebenenfalls unter den ausgeblendeten Symbolen. Unter Linux hängt das Status-Icon von der Desktop-Umgebung ab. Falls kein Icon unterstützt wird, bedienst du Kivanto über das Statusfenster; dessen Schließen beendet dann die App.

| Status | Bedeutung |
| --- | --- |
| Grün | Kivanto läuft. **Im Browser öffnen** bringt dich zur Oberfläche. |
| Gelb | Kivanto startet oder wird beendet. |
| Grau | Kivanto ist gestoppt. |
| Rot | Beim Start oder im Betrieb ist ein Problem aufgetreten. Öffne das Statusfenster. |

Zum vollständigen Beenden wählst du **Kivanto Solo beenden** im Menü des Symbols. Das Schließen des Browserfensters beendet die App nicht.

## Deine Daten und Kosten

Kivanto speichert Projekte und Einstellungen lokal auf deinem Rechner. Wenn du einen Cloud-KI-Anbieter oder einen externen Dienst verbindest, werden die für die jeweilige Anfrage benötigten Inhalte an diesen Dienst gesendet. Welche KI du verwendest, bestimmst du selbst.

**Kivanto Solo ist kostenlos für eine Person auf ihrem persönlich genutzten Rechner – privat oder beruflich.** Eine gemeinsame Installation für mehrere Personen benötigt die Kivanto Server-Edition. Es gelten die beim Download beigefügten Nutzungsbedingungen. Kosten deines KI-Anbieters oder anderer verbundener Dienste sind nicht enthalten.

## Aktualisieren und sichern

Auf macOS heißt die neue App **Kivanto Solo.app**. Beende die bisherige **Kivanto.app**, bevor du wechselst. Nach erfolgreichem Start kannst du die alte App entfernen. Erneuere anschließend bestehende MCP-Verknüpfungen über **KI-Clients verbinden**, damit sie den neuen App-Pfad verwenden. Das gilt auch, wenn sich der Speicherort der portablen Linux-App ändert.

Beende Kivanto vor einem Update und installiere die neue Version. Deine Daten liegen getrennt von der Anwendung. Falls der Assistent nach einem Speicherort fragt, wähle den bisherigen Datenordner.

Für ein Backup beende Kivanto und sichere den **gesamten bei der Einrichtung gewählten Speicherordner**, einschließlich der Datei `kivanto.env`. Direkt eingebundene Originalordner solltest du zusätzlich sichern.

## Wenn etwas nicht funktioniert

- **Die Oberfläche öffnet sich nicht:** Prüfe den Status über das Kivanto-Symbol und wähle **Im Browser öffnen**.
- **Die KI antwortet nicht:** Öffne **KI-Modell einrichten**, prüfe das gewählte Modell und teste die Verbindung. Bei lokaler KI muss auch Ollama beziehungsweise der LM-Studio-Server laufen.
- **Dokumente fehlen in einer Antwort:** Prüfe das ausgewählte Projekt, die hinzugefügten Dateien und den Stand des Einlesevorgangs. Aktualisiere eingebundene Quellen bei Bedarf mit **Synchronisieren**.
- **Du möchtest einen Fehler melden:** Öffne ein [Issue](https://github.com/KardungLa/kivanto-downloads/issues) mit Betriebssystem, Kivanto-Version und einer kurzen Beschreibung der Schritte. Entferne persönliche Inhalte und Zugangsdaten aus Screenshots oder Protokollen vor dem Hochladen.
