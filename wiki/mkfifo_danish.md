# [Linux] Bash mkfifo Brug: Opretter en named pipe

## Oversigt
`mkfifo` er en Bash-kommando, der bruges til at oprette en named pipe (FIFO). En named pipe tillader kommunikation mellem forskellige processer ved at fungere som en midlertidig buffer, hvor data kan skrives til og læses fra.

## Brug
Den grundlæggende syntaks for `mkfifo`-kommandoen er som følger:

```bash
mkfifo [muligheder] [argumenter]
```

## Almindelige muligheder
- `-m, --mode=MODE`: Angiver filrettighederne for den oprettede FIFO.
- `-Z, --context=CONTEXT`: Angiver sikkerhedskonteksten for den oprettede FIFO (kun relevant for SELinux).

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `mkfifo`:

1. Opret en simpel named pipe:
   ```bash
   mkfifo min_fifo
   ```

2. Opret en named pipe med specifikke rettigheder:
   ```bash
   mkfifo -m 644 min_fifo
   ```

3. Opret flere named pipes på én gang:
   ```bash
   mkfifo fifo1 fifo2 fifo3
   ```

4. Opret en named pipe med en specifik sikkerhedskontekst:
   ```bash
   mkfifo -Z my_fifo
   ```

## Tips
- Sørg for at rydde op efter dig selv ved at slette named pipes, når de ikke længere er nødvendige, ved hjælp af `rm`-kommandoen.
- Tjek altid, om en named pipe allerede eksisterer, før du prøver at oprette en ny med samme navn for at undgå fejl.
- Brug named pipes til at forbinde output fra én proces til input af en anden for at lette dataoverførsel.