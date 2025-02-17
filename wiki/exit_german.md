# [Linux] Bash exit Verwendung: Beenden eines Skripts oder einer Shell

## Übersicht
Der `exit` Befehl in Bash wird verwendet, um ein Skript oder eine Shell-Sitzung zu beenden. Er kann auch einen Statuscode zurückgeben, der angibt, ob das Skript erfolgreich ausgeführt wurde oder ob ein Fehler aufgetreten ist.

## Verwendung
Die grundlegende Syntax des `exit` Befehls lautet:

```bash
exit [options] [status]
```

## Häufige Optionen
- `status`: Ein optionaler Parameter, der den Exit-Status angibt. Standardmäßig wird `0` verwendet, was Erfolg bedeutet. Ein Wert ungleich `0` zeigt einen Fehler an.

## Häufige Beispiele

1. **Einfaches Beenden eines Skripts:**
   ```bash
   #!/bin/bash
   echo "Das Skript wird jetzt beendet."
   exit
   ```

2. **Beenden mit einem spezifischen Statuscode:**
   ```bash
   #!/bin/bash
   echo "Ein Fehler ist aufgetreten."
   exit 1
   ```

3. **Verwendung in einer Bedingung:**
   ```bash
   #!/bin/bash
   if [ -f "datei.txt" ]; then
       echo "Datei gefunden."
       exit 0
   else
       echo "Datei nicht gefunden."
       exit 2
   fi
   ```

4. **Beenden einer interaktiven Shell:**
   ```bash
   exit
   ```

## Tipps
- Verwenden Sie `exit 0`, um anzuzeigen, dass ein Skript erfolgreich abgeschlossen wurde.
- Nutzen Sie spezifische Statuscodes (z.B. `exit 1`, `exit 2`), um unterschiedliche Fehlerarten zu kennzeichnen, was die Fehlersuche erleichtert.
- In interaktiven Shells kann `exit` auch verwendet werden, um die Sitzung zu beenden, was nützlich ist, um Ressourcen freizugeben.