# [Linux] Bash printf bruk: Formatert utskrift av tekst

## Oversikt
`printf`-kommandoen brukes til å formatere og skrive ut tekst til standard utgang. Den gir mer kontroll over formatet enn den enklere `echo`-kommandoen, og er nyttig for å lage velstrukturerte utdata.

## Bruk
Den grunnleggende syntaksen for `printf`-kommandoen er som følger:

```bash
printf [alternativer] [argumenter]
```

## Vanlige alternativer
- `-v`: Lagre resultatet i en variabel i stedet for å skrive det ut.
- `-f`: Angi formatet for utskriften.
- `-n`: Unngå å legge til en ny linje på slutten av utskriften.

## Vanlige eksempler

1. **Enkel tekstutskrift:**
   ```bash
   printf "Hei, verden!\n"
   ```

2. **Formatert tallutskrift:**
   ```bash
   printf "Tall: %.2f\n" 3.14159
   ```

3. **Utskrift med flere argumenter:**
   ```bash
   printf "Navn: %s, Alder: %d\n" "Ola" 30
   ```

4. **Lagring av resultat i en variabel:**
   ```bash
   printf -v result "Resultat: %.1f" 9.876
   echo "$result"
   ```

5. **Utskrift uten ny linje:**
   ```bash
   printf "Dette er på samme linje."
   printf " Og dette også."
   ```

## Tips
- Bruk `%.nf` for å spesifisere antall desimaler når du skriver ut flyttall.
- Husk at `printf` ikke automatisk legger til en ny linje, så vær oppmerksom på dette når du formaterer utdata.
- Det kan være nyttig å bruke `printf` i skript for å lage mer lesbare og strukturerte rapporter.