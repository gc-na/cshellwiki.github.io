# [Linux] Bash trap användning: Hantera signaler och städa upp resurser

## Översikt
Kommandot `trap` i Bash används för att fånga och hantera signaler och händelser som kan inträffa under körningen av ett skript. Det gör det möjligt att utföra specifika kommandon när ett skript avslutas, avbryts eller får en viss signal, vilket är särskilt användbart för att städa upp resurser.

## Användning
Den grundläggande syntaxen för kommandot `trap` är:

```bash
trap [options] [arguments]
```

## Vanliga alternativ
- `SIGINT`: Fångar avbrottssignalen (Ctrl+C).
- `EXIT`: Utför kommandon när skriptet avslutas.
- `ERR`: Utför kommandon om ett kommando i skriptet misslyckas.
- `SIGTERM`: Fångar signalen för att avsluta processen.

## Vanliga exempel

### Exempel 1: Fånga avbrottssignal
Detta exempel visar hur man fångar en avbrottssignal och utför en städning innan skriptet avslutas.

```bash
#!/bin/bash

trap 'echo "Avbrott fångat! Städar upp..."; exit' SIGINT

while true; do
    echo "Kör skript... (tryck Ctrl+C för att avbryta)"
    sleep 1
done
```

### Exempel 2: Utföra kommandon vid avslut
I detta exempel används `trap` för att köra ett kommando när skriptet avslutas.

```bash
#!/bin/bash

trap 'echo "Skriptet avslutas..."; rm -f temp.txt' EXIT

echo "Skapar en temporär fil..."
touch temp.txt
sleep 5
```

### Exempel 3: Fånga fel
Detta exempel visar hur man fångar ett fel och utför en åtgärd.

```bash
#!/bin/bash

trap 'echo "Ett fel inträffade!"; exit 1' ERR

echo "Kör ett kommando som misslyckas..."
false  # Detta kommando kommer att misslyckas
```

## Tips
- Använd `trap` för att säkerställa att viktiga städåtgärder alltid utförs, oavsett hur skriptet avslutas.
- Tänk på att `trap` kan användas för att fånga flera signaler genom att separera dem med mellanslag.
- Testa alltid skriptet noggrant för att se till att `trap` fungerar som förväntat, särskilt i produktionsmiljöer.