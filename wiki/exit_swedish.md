# [Linux] Bash exit användning: Avsluta ett skript eller en terminalsession

## Översikt
Kommandot `exit` används för att avsluta ett skript eller en terminalsession i Bash. Det kan också returnera ett statusvärde till det omgivande systemet, vilket kan vara användbart för att indikera om skriptet kördes framgångsrikt eller om det inträffade ett fel.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
exit [options] [status]
```

## Vanliga alternativ
- `status`: Ett heltal som anger avslutningsstatusen. Standardvärdet är 0, vilket indikerar att allt gick bra. Andra värden kan användas för att indikera olika typer av fel.

## Vanliga exempel
Här är några praktiska exempel på hur `exit` kan användas:

1. Avsluta ett skript med standardstatus (0):
    ```bash
    #!/bin/bash
    echo "Skriptet kördes framgångsrikt."
    exit
    ```

2. Avsluta ett skript med en specifik status (1):
    ```bash
    #!/bin/bash
    echo "Ett fel inträffade."
    exit 1
    ```

3. Använda `exit` i en interaktiv terminalsession:
    ```bash
    $ exit
    ```

4. Avsluta ett skript baserat på en villkorssats:
    ```bash
    #!/bin/bash
    if [ -f "fil.txt" ]; then
        echo "Fil finns."
        exit 0
    else
        echo "Fil saknas."
        exit 1
    fi
    ```

## Tips
- Använd alltid ett statusvärde för att indikera resultatet av skriptet, vilket gör det lättare att felsöka.
- Kom ihåg att ett statusvärde på 0 betyder framgång, medan alla andra värden indikerar olika typer av fel.
- Om du kör skriptet i en terminal och vill avsluta sessionen, kan du använda `exit` utan några argument för att stänga terminalfönstret.