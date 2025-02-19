# [Unix] C Shell (csh) foreach Verwendung: Schleifen über eine Liste von Elementen

## Übersicht
Der Befehl `foreach` in der C Shell (csh) ermöglicht es Benutzern, eine Schleife über eine Liste von Elementen auszuführen. Dies ist besonders nützlich, um eine Reihe von Befehlen für jedes Element in der Liste zu wiederholen.

## Verwendung
Die grundlegende Syntax des `foreach`-Befehls lautet:

```
foreach variable (liste)
    befehle
end
```

## Häufige Optionen
- **variable**: Der Name der Variablen, die jedes Element der Liste speichert.
- **liste**: Eine durch Leerzeichen getrennte Liste von Elementen, über die iteriert wird.
- **befehle**: Die Befehle, die für jedes Element in der Liste ausgeführt werden.

## Häufige Beispiele

### Beispiel 1: Einfache Schleife über eine Liste
```csh
foreach i (1 2 3 4 5)
    echo "Zahl: $i"
end
```
Dieses Beispiel gibt die Zahlen 1 bis 5 aus.

### Beispiel 2: Schleife über Dateinamen
```csh
foreach file (*.txt)
    echo "Verarbeite Datei: $file"
end
```
Hier wird jede `.txt`-Datei im aktuellen Verzeichnis verarbeitet.

### Beispiel 3: Schleife mit Befehlen
```csh
foreach dir (dir1 dir2 dir3)
    cd $dir
    ls
    cd ..
end
```
In diesem Beispiel wird in jedes Verzeichnis gewechselt, der Inhalt aufgelistet und dann zurück ins ursprüngliche Verzeichnis gewechselt.

## Tipps
- Verwenden Sie `@`-Befehle innerhalb der Schleife, um Variablen zu manipulieren.
- Achten Sie darauf, die Schleife mit `end` zu beenden, um Syntaxfehler zu vermeiden.
- Nutzen Sie Platzhalter wie `*` oder `?`, um mehrere Dateien oder Verzeichnisse in einer Schleife zu verarbeiten.