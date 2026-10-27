# TDevTools

**Ein kostenloses Desktop-Toolkit für Entwickler: 47 Werkzeuge für JSON, XML, Schemas, APIs, Kodierung und Zertifikate, für macOS, Windows und Linux.**

Von [transposal.app](https://transposal.app)

**Lesen auf:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 Läuft lokal. Deine Daten verlassen niemals deinen Computer.** TDevTools verarbeitet alles auf deinem Rechner. JSON- und XML-Dateien, Tokens, Schlüssel und Zertifikate werden weder hochgeladen noch an Analysedienste gesendet. Es gibt keine Konten und kein Tracking. Die App verbindet sich nur dann mit dem Internet, wenn du es ausdrücklich veranlasst: beim Laden einer URL, beim Senden einer Testanfrage an deine API oder beim Abrufen eines Serverzertifikats. Alle übrigen Werkzeuge funktionieren offline.

## Screenshots

**JSON → JSON Schema:** Schema aus Beispieldaten ableiten.

![JSON zu JSON Schema](screenshots/json-to-schema.png)

**API-Tester:** Anfragen senden und Antworten als Baum, Tabelle oder Text anzeigen.

![API-Tester](screenshots/api-tester.png)

**Zertifikats-Inspektor:** Zertifikatskette anzeigen und Zertifikate sowie Signaturen prüfen.

![Zertifikats-Inspektor](screenshots/certificate-inspector.png)

## Download

Die neueste Version findest du auf der [Release-Seite](https://github.com/siddiquin/TDevTools-releases/releases/latest).

| System | Download-Datei |
| --- | --- |
| macOS, Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS, Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11, 64-Bit | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11, ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows, portabel | `TDevTools-Portable-<version>.exe` |
| Linux, 64-Bit (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux, ARM64 | `TDevTools-<version>-arm64.AppImage` |

**Systemvoraussetzungen:** macOS 12 Monterey oder neuer; Windows 10 oder 11 (64-Bit oder ARM64); oder eine aktuelle 64-Bit-Linux-Distribution (Ubuntu 20.04+, Debian 11+, Fedora 36+ oder ähnlich). Etwa 300 MB freier Speicherplatz.

## Installation

### macOS

1. Lade die passende `.dmg`-Datei herunter, öffne sie und stimme der Lizenz zu.
2. Ziehe **TDevTools** in den Ordner **Programme** und wirf das Disk-Image aus.
3. Beim ersten Start kann macOS warnen, dass die App nicht überprüft werden kann, weil sie nicht mit einem kostenpflichtigen Apple-Developer-Zertifikat signiert ist. Das ist erwartbar; du musst die App nur einmal freigeben.
   - **macOS 14 oder älter:** Klicke im Finder mit der rechten Maustaste auf TDevTools, wähle **Öffnen** und bestätige erneut.
   - **macOS 15 oder neuer:** Versuche, die App zu öffnen, und klicke in der Warnung auf **Fertig**. Öffne **Systemeinstellungen → Datenschutz & Sicherheit** und klicke neben der TDevTools-Sperrmeldung auf **Dennoch öffnen**. Bestätige.
4. Wenn macOS meldet, TDevTools sei beschädigt, prüfe zuerst, dass der Download von der offiziellen [Release-Seite](https://github.com/siddiquin/TDevTools-releases/releases/latest) stammt. Führe anschließend im Terminal `xattr -dr com.apple.quarantine /Applications/TDevTools.app` aus, um nur bei dieser App die Quarantäne-Markierung zu entfernen.

### Windows

- **Installer:** Starte `TDevTools-Setup-<version>-x64.exe` (für ARM-PCs die `arm64`-Datei), akzeptiere die Lizenz und klicke auf **Installieren**. Meldet SmartScreen „Windows hat Ihren PC geschützt“, wähle **Weitere Informationen → Trotzdem ausführen**. Die Installation gilt nur für dein Benutzerkonto und benötigt keine Administratorrechte.
- **Portable Version:** Starte `TDevTools-Portable-<version>.exe`. Bei SmartScreen wähle **Weitere Informationen → Trotzdem ausführen**.

### Linux (AppImage)

Lade die passende Datei herunter und erlaube die Ausführung unter **Eigenschaften → Berechtigungen** oder mit `chmod +x TDevTools-*.AppImage`. Öffne sie anschließend oder starte sie im Terminal. Falls sie nicht startet, benötigt manche Distribution FUSE 2 (Ubuntu/Debian: `sudo apt install libfuse2`; Ubuntu 24.04: `sudo apt install libfuse2t64`; Fedora: `sudo dnf install fuse-libs`). Gear Lever oder AppImageLauncher kann einen Menüeintrag anlegen.

## Aktualisieren und Deinstallieren

Lade zum Aktualisieren die neue Version herunter und installiere sie wie zuvor; deine Einstellungen bleiben erhalten. Unter macOS ersetzt du die App in Programme, unter Windows startest du den neuen Installer und unter Linux ersetzt du die AppImage-Datei.

- **macOS:** Ziehe TDevTools in den Papierkorb. Für eine vollständige Entfernung der Einstellungen lösche `~/Library/Application Support/TDevTools`.
- **Windows:** Deinstalliere TDevTools unter **Einstellungen → Apps → Installierte Apps**. Für die Einstellungen lösche `%APPDATA%\TDevTools`. Bei der portablen Version genügt es, die `.exe` zu löschen.
- **Linux:** Lösche die AppImage-Datei. Für die Einstellungen lösche `~/.config/TDevTools`.

Die App speichert nur Einstellungen wie Design und Sprache, keine Kopien deiner Daten, Passwörter oder Schlüssel.

## Funktionen

- **Formatieren und validieren:** JSON formatieren, prüfen, reparieren und visuell bearbeiten; JSON, XML, CSV, Excel, YAML, TOON und JSONL konvertieren; Markdown und JSON-/XML-Schemas (XSD); TypeScript-Typen generieren.
- **Sicherheit:** JWT decodieren, verifizieren und signieren; Base64-, URL- und SAML-Kodierung; MD5-, SHA-1- und SHA-256-Hashes; selbstsignierte Zertifikate und mTLS-Kits erstellen; Zertifikate, öffentliche Schlüssel und JKS-Keystores prüfen.
- **Anzeigen und APIs:** JSON als Baum, Tabelle, Raster, Graph oder Rohtext; OpenAPI-/Swagger-Browser, HTTP-Client mit OAuth2 und mTLS, SOAP-/WSDL-Viewer, Datei-Viewer und Markdown-Vorschau.
- **Abfragen und Transformationen:** JSONPath-Tester, Suche und Ersetzen mit regulären Ausdrücken, JSON-Zuordnung mit Export nach JavaScript, TypeScript, Python oder C#; optionaler Cloud-Dienst Transposal Mapper.
- **Vergleichen:** strukturelle Unterschiede in JSON/XML und JSON-Schema-Prüfung mit zeilenbezogenen Fehlern.
- **Überall in der App:** 8 Sprachen, 6 Designs, Akzentfarben, Dichte und Zoom, Kopieren per Schaltfläche, Kontextmenü, Drag-and-drop sowie CPU- und Speicherauslastung in der Statusleiste.

## Datenschutz und Sicherheit

- Jede Verarbeitung findet lokal statt. Eingefügte oder geöffnete Daten werden nicht hochgeladen.
- Keine Konten, Telemetrie oder Werbung.
- Netzwerkverbindungen nur auf deine Anfrage, etwa beim Laden einer URL, Testen einer API oder Abrufen eines Zertifikats.
- Passwörter, Tokens und private Schlüssel bleiben nur während der Laufzeit im Speicher; gespeichert werden ausschließlich deine Einstellungen.
- Abgeschottete Fenster und strenge Content-Security-Policy; HTML-Vorschauen führen keine Skripte aus; vor dem Öffnen von Programmen oder Skripten fragt die App nach; Anmeldedaten gehen nur an den ausgewählten Server.
- Die integrierten Beispiele verwenden öffentliche Demo-Server und sind auf eine Anfrage alle 2 Minuten begrenzt. Für eigene URLs und Dateien gilt kein Limit.

## Häufige Fragen

**Ist TDevTools kostenlos?** Ja, für Entwickler ist es kostenlos. Siehe die [Lizenzvereinbarung](LICENSE.md).

**Funktioniert es offline?** Ja, außer bei Funktionen, die mit einem von dir ausgewählten Server kommunizieren (URL laden, API-/SOAP-Testanfragen, Zertifikatskette abrufen).

**Ist der Quellcode verfügbar?** TDevTools ist proprietär. Du kannst den Quellcode per E-Mail an **<support@transposal.app>** mit dem Betreff „TDevTools“ anfragen.

**Warum warnt mein Computer bei der Installation?** Die App ist nicht mit einem kostenpflichtigen Apple- oder Microsoft-Entwicklerzertifikat signiert. Gatekeeper und SmartScreen zeigen deshalb beim ersten Start eine Warnung. Folge den Installationsschritten und lade TDevTools ausschließlich von der offiziellen [Release-Seite](https://github.com/siddiquin/TDevTools-releases/releases/latest) herunter.

## Lizenz und Support

- [Endbenutzer-Lizenzvereinbarung](LICENSE.md): kostenlose Nutzung, ohne Gewährleistung. Die vollständige Vereinbarung ist in 8 Sprachen unter **Hilfe → Lizenzvereinbarung** in der App verfügbar.
- [Hinweise zu Drittanbietern](THIRD_PARTY_NOTICES.md)
- Support: **<support@transposal.app>**
- Website: [transposal.app](https://transposal.app)

© 2026 Transposal. Alle Rechte vorbehalten.