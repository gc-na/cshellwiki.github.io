# [Linux] Bash stat Verwendung: Anzeige von Dateiinformationen

## Übersicht
Der `stat` Befehl wird verwendet, um detaillierte Informationen über Dateien und Verzeichnisse im Dateisystem anzuzeigen. Dazu gehören unter anderem die Größe, die Berechtigungen, die Zeitstempel und der Dateityp.

## Verwendung
Die grundlegende Syntax des `stat` Befehls lautet:

```bash
stat [Optionen] [Argumente]
```

## Häufige Optionen
- `-c` : Benutzerdefiniertes Format für die Ausgabe.
- `-f` : Informationen über das Dateisystem, in dem die Datei gespeichert ist.
- `--format` : Ermöglicht die Angabe eines Formats für die Ausgabe.
- `-t` : Ausgabe in einem kompakten, tabellarischen Format.

## Häufige Beispiele
Um die Informationen einer Datei anzuzeigen, verwenden Sie:

```bash
stat dateiname.txt
```

Um die Informationen im benutzerdefinierten Format anzuzeigen:

```bash
stat -c '%s %y' dateiname.txt
```

Um Informationen über das Dateisystem zu erhalten:

```bash
stat -f dateiname.txt
```

Um die Ausgabe im tabellarischen Format anzuzeigen:

```bash
stat -t dateiname.txt
```

## Tipps
- Verwenden Sie die `-c` Option, um nur die benötigten Informationen anzuzeigen und die Ausgabe zu vereinfachen.
- Kombinieren Sie `stat` mit anderen Befehlen wie `grep`, um spezifische Informationen zu filtern.
- Nutzen Sie die `--format` Option, um die Ausgabe an Ihre Bedürfnisse anzupassen und leserlicher zu gestalten.