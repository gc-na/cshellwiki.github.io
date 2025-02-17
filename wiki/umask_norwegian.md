# [Linux] Bash umask Bruk: Angir standard tillatelser for nye filer og kataloger

## Oversikt
`umask`-kommandoen brukes til å angi standard tillatelser for nye filer og kataloger som opprettes i Unix-lignende operativsystemer. Den definerer hvilke tillatelser som skal fjernes fra de standard tillatelsene som tildeles av systemet.

## Bruk
Den grunnleggende syntaksen for `umask`-kommandoen er som følger:

```bash
umask [alternativer] [argumenter]
```

## Vanlige alternativer
- `-S`: Viser umask-verdien i symbolsk form.
- `-p`: Viser den nåværende umask-verdien i et format som kan brukes i skript.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `umask`:

1. **Sjekk nåværende umask-verdi:**
   ```bash
   umask
   ```

2. **Sett umask til 022:**
   Dette vil fjerne skrive- og utføre-tillatelser for gruppen og andre.
   ```bash
   umask 022
   ```

3. **Sett umask til 007:**
   Dette vil fjerne alle tillatelser for andre og gi full tilgang til eieren og gruppen.
   ```bash
   umask 007
   ```

4. **Vis umask i symbolsk form:**
   ```bash
   umask -S
   ```

5. **Bruk umask i et skript:**
   Du kan sette umask i et skript for å kontrollere tillatelser for filer som opprettes av skriptet.
   ```bash
   #!/bin/bash
   umask 027
   touch ny_fil.txt
   ```

## Tips
- Vær oppmerksom på at umask-verdien er en maske som reduserer tillatelser; for eksempel, en umask på 022 gir 755 tillatelser for kataloger og 644 for filer.
- Det kan være nyttig å sette umask i brukerens shell-konfigurasjonsfil (som `.bashrc` eller `.bash_profile`) for å sikre at ønskede tillatelser alltid brukes.
- Test umask-innstillingene dine ved å opprette filer og kataloger for å se hvilke tillatelser som faktisk blir tildelt.