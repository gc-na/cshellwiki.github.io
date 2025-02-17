# [Linux] Bash chage brug: Administrer brugerens adgangskodeudløb

## Oversigt
`chage`-kommandoen bruges til at ændre indstillingerne for adgangskodeudløb for brugerkonti i Linux. Det giver systemadministratorer mulighed for at styre, hvornår en bruger skal ændre sin adgangskode, og hvor længe en adgangskode forbliver gyldig.

## Brug
Den grundlæggende syntaks for `chage`-kommandoen er:

```bash
chage [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l, --list`: Vis oplysninger om adgangskodeudløb for en bruger.
- `-m, --mindays`: Angiv minimum antal dage mellem adgangskodeændringer.
- `-M, --maxdays`: Angiv maksimum antal dage, en adgangskode er gyldig.
- `-I, --inactive`: Angiv antal dage, en konto forbliver aktiv efter adgangskodeudløb.
- `-E, --expire`: Angiv en dato, hvor kontoen udløber.

## Almindelige eksempler
1. For at vise adgangskodeudløbsoplysninger for brugeren `john`:
   ```bash
   chage -l john
   ```

2. For at indstille minimum antal dage mellem adgangskodeændringer til 5 dage for brugeren `john`:
   ```bash
   chage -m 5 john
   ```

3. For at indstille maksimum antal dage, en adgangskode kan være gyldig til 90 dage for brugeren `john`:
   ```bash
   chage -M 90 john
   ```

4. For at indstille kontoen til at udløbe 30 dage efter adgangskodeudløb for brugeren `john`:
   ```bash
   chage -I 30 john
   ```

5. For at indstille en udløbsdato for kontoen til den 1. januar 2024 for brugeren `john`:
   ```bash
   chage -E 2024-01-01 john
   ```

## Tips
- Sørg for at kontrollere adgangskodepolitikken i din organisation, før du ændrer indstillingerne.
- Brug `chage -l [bruger]` regelmæssigt for at overvåge adgangskodeudløb og sikre, at brugerne overholder politikkerne.
- Overvej at indstille påmindelser til brugerne, så de er opmærksomme på kommende adgangskodeændringer.