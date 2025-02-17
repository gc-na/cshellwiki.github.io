# [Linux] Bash trap bruk: Håndter signaler og rensing av ressurser

## Oversikt
`trap`-kommandoen i Bash brukes til å håndtere signaler og utføre spesifikke handlinger når et skript mottar et signal. Dette kan være nyttig for å rydde opp i ressurser eller utføre bestemte oppgaver før skriptet avsluttes.

## Bruk
Den grunnleggende syntaksen for `trap`-kommandoen er som følger:

```bash
trap [handling] [signal]
```

## Vanlige alternativer
- `EXIT`: Utfør handlingen når skriptet avsluttes.
- `SIGINT`: Utfør handlingen når skriptet mottar et avbruddssignal (Ctrl+C).
- `SIGTERM`: Utfør handlingen når skriptet mottar et terminering signal.
- `SIGQUIT`: Utfør handlingen når skriptet mottar et signal for å avslutte (Ctrl+\).

## Vanlige eksempler

### Eksempel 1: Rydde opp ved avslutning
Dette eksemplet viser hvordan man kan bruke `trap` for å rydde opp i midlertidige filer når skriptet avsluttes.

```bash
#!/bin/bash
trap 'rm -f /tmp/mytempfile' EXIT
touch /tmp/mytempfile
echo "Skriptet kjører..."
```

### Eksempel 2: Håndtere avbrudd
Her er et eksempel på hvordan man kan håndtere et avbruddssignal (Ctrl+C) for å vise en melding.

```bash
#!/bin/bash
trap 'echo "Skriptet ble avbrutt!"' SIGINT
while true; do
    echo "Skriptet kjører. Trykk Ctrl+C for å avbryte."
    sleep 1
done
```

### Eksempel 3: Rydde opp ved terminering
I dette eksemplet vil skriptet rydde opp i ressurser når det mottar et terminering signal.

```bash
#!/bin/bash
trap 'echo "Rydder opp..."; exit' SIGTERM
while true; do
    echo "Skriptet kjører. Send SIGTERM for å avslutte."
    sleep 1
done
```

## Tips
- Bruk `trap` for å sikre at viktige ressurser alltid blir ryddet opp, selv om skriptet avbrytes uventet.
- Test skriptene dine for å se hvordan de reagerer på forskjellige signaler.
- Vær oppmerksom på rekkefølgen av `trap`-kommandoene, da den første som matcher signalet vil bli utført.