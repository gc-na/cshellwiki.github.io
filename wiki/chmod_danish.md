# [Linux] Bash chmod brug: Ændre filrettigheder

## Oversigt
`chmod` (change mode) er en Bash-kommando, der bruges til at ændre fil- og mappetilladelser i Unix-lignende operativsystemer. Denne kommando gør det muligt for brugere at kontrollere, hvem der kan læse, skrive eller udføre en fil.

## Brug
Den grundlæggende syntaks for `chmod`-kommandoen er som følger:

```bash
chmod [muligheder] [argumenter]
```

## Almindelige muligheder
- `u`: Ændrer tilladelser for ejeren af filen (user).
- `g`: Ændrer tilladelser for gruppen, som ejeren tilhører (group).
- `o`: Ændrer tilladelser for andre brugere (others).
- `r`: Giver læsetilladelse (read).
- `w`: Giver skrivetilladelse (write).
- `x`: Giver udførelsestilladelse (execute).
- `+`: Tilføjer en tilladelse.
- `-`: Fjerner en tilladelse.
- `=`: Sætter tilladelserne til en specifik værdi.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `chmod` kan bruges:

1. Giv ejeren læse-, skrive- og udførelsestilladelser, mens gruppen og andre kun får læsetilladelse:
   ```bash
   chmod 744 filnavn
   ```

2. Tilføj udførelsestilladelse for gruppen:
   ```bash
   chmod g+x filnavn
   ```

3. Fjern skrivetilladelse for andre:
   ```bash
   chmod o-w filnavn
   ```

4. Sæt tilladelser, så kun ejeren kan læse og skrive, og ingen andre har tilladelser:
   ```bash
   chmod 600 filnavn
   ```

5. Giv alle brugere læse- og udførelsestilladelse:
   ```bash
   chmod a+rx filnavn
   ```

## Tips
- Brug `ls -l` for at kontrollere de nuværende tilladelser på filer og mapper.
- Vær forsigtig med at give for brede tilladelser, især udførelsestilladelser, da det kan føre til sikkerhedsproblemer.
- Du kan bruge `chmod` med `-R` for at ændre tilladelser rekursivt i en mappe:
  ```bash
  chmod -R 755 mappenavn
  ```