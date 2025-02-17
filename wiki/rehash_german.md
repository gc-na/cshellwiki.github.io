# [Linux] Bash rehash Verwendung: Aktualisiert den Befehlsspeicher

## Übersicht
Der `rehash` Befehl in Bash wird verwendet, um den internen Befehlsspeicher zu aktualisieren. Wenn neue Programme oder Skripte in Verzeichnissen hinzugefügt werden, die im `PATH` enthalten sind, sorgt `rehash` dafür, dass diese neuen Befehle erkannt und verwendet werden können.

## Verwendung
Die grundlegende Syntax des `rehash` Befehls ist:

```bash
rehash [Optionen] [Argumente]
```

## Häufige Optionen
Der `rehash` Befehl hat keine speziellen Optionen, da er in der Regel ohne zusätzliche Parameter verwendet wird.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `rehash`:

1. **Einfaches Rehashing**: Aktualisieren des Befehlsspeichers, um neue Befehle zu erkennen.
   ```bash
   rehash
   ```

2. **Nach Installation eines neuen Programms**: Nach der Installation eines neuen Programms, um sicherzustellen, dass es im Befehlsspeicher verfügbar ist.
   ```bash
   sudo apt install neuer-befehl
   rehash
   ```

3. **Nach dem Hinzufügen eines neuen Verzeichnisses zum PATH**: Wenn ein neues Verzeichnis zum `PATH` hinzugefügt wurde, um die Befehle darin verfügbar zu machen.
   ```bash
   export PATH=$PATH:/neuer/pfad
   rehash
   ```

## Tipps
- Verwenden Sie `rehash` regelmäßig, insbesondere nach der Installation neuer Software oder dem Hinzufügen von Verzeichnissen zum `PATH`.
- Beachten Sie, dass einige Shells wie `bash` automatisch den Befehlsspeicher aktualisieren, sodass `rehash` möglicherweise nicht immer erforderlich ist.
- Wenn Sie häufig neue Skripte erstellen, kann es hilfreich sein, `rehash` in Ihre Shell-Startdateien (z.B. `.bashrc`) aufzunehmen, um sicherzustellen, dass neue Befehle immer verfügbar sind.