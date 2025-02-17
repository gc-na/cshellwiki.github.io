# [Linux] Bash unexpand brug: Konverterer mellem tabulatorer og mellemrum

## Oversigt
`unexpand` er et Bash-kommando, der bruges til at konvertere mellemrum til tabulatorer i tekstfiler. Dette kan være nyttigt, når man arbejder med filer, der kræver en bestemt formatering, eller når man ønsker at reducere filstørrelsen ved at erstatte flere mellemrum med tabulatorer.

## Brug
Den grundlæggende syntaks for `unexpand`-kommandoen er som følger:

```bash
unexpand [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`, `--all`: Konverter alle mellemrum til tabulatorer.
- `-t, --tabs=N`: Angiv bredden af tabulatorer til N antal mellemrum.
- `--help`: Vis hjælp og afslut.
- `--version`: Vis versionsinformation og afslut.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `unexpand`:

1. **Konvertere mellemrum til tabulatorer i en fil:**
   ```bash
   unexpand fil.txt
   ```

2. **Gem output i en ny fil:**
   ```bash
   unexpand fil.txt > ny_fil.txt
   ```

3. **Konvertere alle mellemrum til tabulatorer:**
   ```bash
   unexpand -a fil.txt
   ```

4. **Angive tabulatorbredde til 4 mellemrum:**
   ```bash
   unexpand -t 4 fil.txt
   ```

## Tips
- Brug `unexpand` i kombination med `cat` for at se ændringerne direkte i terminalen:
  ```bash
  cat fil.txt | unexpand
  ```
- Vær opmærksom på, at `unexpand` kun ændrer mellemrum til tabulatorer, hvis det er muligt. Hvis der er en uensartet mængde mellemrum, vil det ikke altid konvertere dem alle.
- Test altid dine ændringer med en kopi af filen, så du ikke mister data ved utilsigtede ændringer.