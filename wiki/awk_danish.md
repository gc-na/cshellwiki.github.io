# [Linux] Bash awk brug: Behandling af tekst og data

## Oversigt
`awk` er et kraftfuldt tekstbehandlingsværktøj, der bruges til at analysere og manipulere data i tekstfiler. Det er især nyttigt til at udtrække specifik information fra strukturerede data, såsom CSV-filer eller logfiler.

## Brug
Den grundlæggende syntaks for `awk` er som følger:

```bash
awk [options] [arguments]
```

## Almindelige muligheder
- `-F`: Angiver feltseparatoren (standard er mellemrum).
- `-v`: Definerer en variabel, der kan bruges i scriptet.
- `-f`: Angiver en fil, der indeholder `awk`-programmet.
- `BEGIN`: En blok, der køres før behandling af inputdata.
- `END`: En blok, der køres efter behandling af inputdata.

## Almindelige eksempler

1. **Udskrivning af specifikke felter fra en fil:**
   For at udskrive det første og tredje felt fra en fil, hvor felterne er adskilt af mellemrum:
   ```bash
   awk '{print $1, $3}' fil.txt
   ```

2. **Brug af en brugerdefineret feltseparator:**
   Hvis du har en CSV-fil og vil udskrive det andet felt:
   ```bash
   awk -F, '{print $2}' fil.csv
   ```

3. **Beregning af summen af en kolonne:**
   For at beregne summen af værdierne i den tredje kolonne:
   ```bash
   awk '{sum += $3} END {print sum}' fil.txt
   ```

4. **Filtrering af linjer baseret på betingelse:**
   For at udskrive linjer, hvor det første felt er lig med "A":
   ```bash
   awk '$1 == "A"' fil.txt
   ```

## Tips
- Brug `-F` til at ændre feltseparatoren, når du arbejder med forskellige dataformater.
- Tjek `awk`-manualen (`man awk`) for at få en dybere forståelse af de tilgængelige funktioner og muligheder.
- Overvej at bruge `BEGIN` og `END` blokke til at udføre initialisering og opsummering af data.