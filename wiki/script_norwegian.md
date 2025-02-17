# [Linux] Bash script Bruk: Ta opp terminaløkter

## Oversikt
`script`-kommandoen brukes til å ta opp en terminaløkt. Den lagrer alt som vises i terminalvinduet i en fil, noe som er nyttig for dokumentasjon eller feilsøking.

## Bruk
Den grunnleggende syntaksen for `script`-kommandoen er som følger:

```bash
script [alternativer] [filnavn]
```

## Vanlige alternativer
- `-a`: Legger til innholdet i den eksisterende filen i stedet for å overskrive den.
- `-q`: Kjør i stille modus, som ikke viser start- og sluttmeldinger.
- `-t`: Lag en tidslogg av terminaløkten.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `script`-kommandoen:

1. Ta opp en terminaløkt til en fil som heter `output.txt`:
   ```bash
   script output.txt
   ```

2. Ta opp en terminaløkt og legg til innholdet i en eksisterende fil:
   ```bash
   script -a output.txt
   ```

3. Kjør `script` i stille modus:
   ```bash
   script -q output.txt
   ```

4. Ta opp en terminaløkt og lag en tidslogg:
   ```bash
   script -t output.txt
   ```

## Tips
- Husk å avslutte `script`-økten ved å skrive `exit` eller trykke `Ctrl+D` for å sikre at filen lukkes riktig.
- Sjekk innholdet i den opprettede filen med `cat` eller `less` for å se hva som ble registrert.
- Bruk `script` i kombinasjon med andre kommandoer for å dokumentere spesifikke prosesser eller feilsøkingsøkter.