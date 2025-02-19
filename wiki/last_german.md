# [Linux] C Shell (csh) last Befehl: Zeigt die letzten Anmeldungen an

## Übersicht
Der `last` Befehl zeigt eine Liste der letzten Anmeldungen von Benutzern auf dem System an. Er nutzt die Datei `/var/log/wtmp`, um Informationen über Anmeldungen, Abmeldungen und Systemstarts bereitzustellen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
last [Optionen] [Argumente]
```

## Häufige Optionen
- `-n [anzahl]`: Gibt die letzten `anzahl` Anmeldungen aus.
- `-R`: Unterdrückt die Anzeige von Hostnamen.
- `-f [datei]`: Gibt eine alternative wtmp-Datei an, um die Anmeldungen zu lesen.

## Häufige Beispiele
Um die letzten 10 Anmeldungen anzuzeigen, verwenden Sie:

```bash
last -n 10
```

Um die letzten Anmeldungen ohne Hostnamen anzuzeigen, verwenden Sie:

```bash
last -R
```

Um Anmeldungen aus einer bestimmten wtmp-Datei anzuzeigen, verwenden Sie:

```bash
last -f /pfad/zur/wtmp
```

## Tipps
- Nutzen Sie die Option `-n`, um die Ausgabe zu begrenzen und nur die relevantesten Informationen anzuzeigen.
- Überprüfen Sie regelmäßig die Anmeldungen, um unbefugte Zugriffe zu erkennen.
- Kombinieren Sie `last` mit anderen Befehlen wie `grep`, um spezifische Benutzeranmeldungen zu filtern.