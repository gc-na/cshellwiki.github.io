# [Linux] Bash mkfifo Bruk: Opprett en FIFO (named pipe)

## Oversikt
`mkfifo` er en Bash-kommando som brukes til å opprette en FIFO (First In, First Out) fil, også kjent som en named pipe. Denne typen fil lar prosesser kommunisere med hverandre ved å sende data i en sekvensiell rekkefølge.

## Bruk
Grunnleggende syntaks for `mkfifo`-kommandoen er som følger:

```bash
mkfifo [alternativer] [filnavn]
```

## Vanlige alternativer
- `-m, --mode=MODUS`: Angir tillatelsene for den opprettede FIFO-filen.
- `-Z, --context=KONTEKST`: Setter sikkerhetskonteksten for den opprettede FIFO-filen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mkfifo`:

### Opprett en enkel FIFO
For å opprette en FIFO-fil kalt `min_fifo`, kan du bruke følgende kommando:

```bash
mkfifo min_fifo
```

### Opprett en FIFO med spesifikke tillatelser
For å opprette en FIFO-fil med spesifikke tillatelser (for eksempel 644), kan du bruke:

```bash
mkfifo -m 644 min_fifo
```

### Bruke FIFO med prosesser
Du kan bruke FIFO til å sende data mellom prosesser. For eksempel, i ett terminalvindu kan du skrive:

```bash
cat < min_fifo
```

Og i et annet terminalvindu kan du sende data til FIFO-filen:

```bash
echo "Hei, verden!" > min_fifo
```

## Tips
- Husk at FIFO-filer blokkerer leseren til data er tilgjengelig. Sørg for at det alltid er en prosess som leser fra FIFO-filen.
- Bruk `ls -l` for å sjekke tillatelsene til FIFO-filen etter opprettelse.
- Du kan bruke FIFO-filer for å synkronisere prosesser i skript for å forbedre kommunikasjonen mellom dem.