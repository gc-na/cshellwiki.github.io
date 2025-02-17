# [Linux] Bash mkfifo användning: Skapa namngivna rör

## Översikt
`mkfifo` är ett Bash-kommando som används för att skapa namngivna rör (FIFO - First In, First Out). Dessa rör möjliggör kommunikation mellan olika processer i Unix-liknande operativsystem.

## Användning
Den grundläggande syntaxen för `mkfifo` är:

```bash
mkfifo [alternativ] [argument]
```

## Vanliga alternativ
- `-m, --mode=MODE`: Sätt behörigheterna för den skapade FIFO-filen.
- `--help`: Visa hjälpmeddelande för kommandot.
- `--version`: Visa versionsinformation för `mkfifo`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mkfifo`:

### Skapa ett enkelt namngivet rör
```bash
mkfifo mitt_ror
```

### Skapa ett rör med specifika behörigheter
```bash
mkfifo -m 644 mitt_ror
```

### Använda ett rör för kommunikation mellan processer
Öppna två terminaler. I den första terminalen, skriv:
```bash
cat mitt_ror
```
I den andra terminalen, skriv:
```bash
echo "Hej från den andra terminalen!" > mitt_ror
```

### Ta bort ett rör
För att ta bort ett rör som skapats med `mkfifo`, använd `rm`-kommandot:
```bash
rm mitt_ror
```

## Tips
- Kontrollera alltid att namnet på det rör du skapar inte redan används av en annan fil eller process.
- Använd `ls -l` för att se behörigheterna för ditt rör efter att du har skapat det.
- Tänk på att FIFO-filer fungerar bäst när de används med processer som körs samtidigt.