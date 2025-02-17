# [Linux] Bash stat brug: Vis filstatistik

## Oversigt
`stat`-kommandoen bruges til at vise detaljerede oplysninger om filer og filsystemobjekter. Den giver brugeren information som filstørrelse, adgangsrettigheder, ejerskab og tidsstempler for ændringer.

## Brug
Den grundlæggende syntaks for `stat`-kommandoen er som følger:

```bash
stat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c` : Angiv et format for output.
- `-f` : Vis oplysninger om filsystemet, hvor filen er placeret.
- `--format` : Specifik format for output, kan bruges i stedet for `-c`.
- `-L` : Følg symboliske links for at vise oplysninger om den fil, de peger på.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `stat`:

1. Vis grundlæggende oplysninger om en fil:
   ```bash
   stat filnavn.txt
   ```

2. Vis oplysninger om en fil med et specifikt format:
   ```bash
   stat -c '%n: %s bytes' filnavn.txt
   ```

3. Vis oplysninger om filsystemet, hvor filen er placeret:
   ```bash
   stat -f filnavn.txt
   ```

4. Følg et symbolsk link og vis oplysninger om den fil, det peger på:
   ```bash
   stat -L linktilfil
   ```

## Tips
- Brug `-c`-muligheden for at tilpasse output, så det kun viser de oplysninger, du har brug for.
- Hvis du arbejder med mange filer, kan du bruge `stat` i kombination med `find` for at få oplysninger om flere filer ad gangen.
- Vær opmærksom på, at `stat` kan vise forskellige oplysninger afhængigt af filsystemet og filens tilstand.