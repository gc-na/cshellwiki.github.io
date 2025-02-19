# [Linux] C Shell (csh) top Befehl: Zeigt laufende Prozesse an

## Übersicht
Der `top` Befehl ist ein leistungsstarkes Werkzeug zur Überwachung von Systemprozessen in Echtzeit. Er zeigt eine dynamische Ansicht der aktuell laufenden Prozesse und deren Ressourcenverbrauch, wie CPU- und Speicherauslastung.

## Verwendung
Die grundlegende Syntax des `top` Befehls lautet:

```csh
top [Optionen] [Argumente]
```

## Häufige Optionen
- `-d <Sekunden>`: Legt das Intervall in Sekunden fest, in dem die Anzeige aktualisiert wird.
- `-p <PID>`: Zeigt nur die Prozesse mit der angegebenen Prozess-ID (PID) an.
- `-u <Benutzer>`: Filtert die Anzeige nach Prozessen, die von einem bestimmten Benutzer ausgeführt werden.

## Häufige Beispiele
Um die Prozesse mit einer Aktualisierungsrate von 2 Sekunden anzuzeigen:

```csh
top -d 2
```

Um nur den Prozess mit der PID 1234 anzuzeigen:

```csh
top -p 1234
```

Um die Prozesse eines bestimmten Benutzers, z.B. "max", anzuzeigen:

```csh
top -u max
```

## Tipps
- Verwenden Sie die `h`-Taste innerhalb von `top`, um Hilfe zu den verfügbaren Befehlen und Optionen zu erhalten.
- Drücken Sie `q`, um die `top`-Anzeige zu beenden.
- Nutzen Sie die Sortierfunktionen, indem Sie die entsprechenden Tasten drücken (z.B. `P` für CPU-Nutzung oder `M` für Speichernutzung), um die Prozesse nach Ihren Bedürfnissen zu organisieren.