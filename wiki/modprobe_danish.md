# [Linux] Bash modprobe brug: Indlæser og fjerner kernelmoduler

## Oversigt
`modprobe` er et Bash-kommando, der bruges til at indlæse og fjerne kernelmoduler i Linux. Det håndterer afhængigheder mellem moduler og sikrer, at de nødvendige moduler indlæses korrekt.

## Brug
Den grundlæggende syntaks for `modprobe` er som følger:

```bash
modprobe [options] [arguments]
```

## Almindelige muligheder
- `-r`, `--remove`: Fjerner et modul fra kernen.
- `-n`, `--dry-run`: Viser, hvad der ville blive gjort, uden at udføre handlingen.
- `-v`, `--verbose`: Viser detaljerede oplysninger om, hvad der sker under indlæsning eller fjernelse af moduler.
- `--show`: Viser, hvilke moduler der ville blive indlæst, uden at indlæse dem.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `modprobe`:

1. Indlæsning af et modul:
   ```bash
   modprobe nvidia
   ```

2. Fjernelse af et modul:
   ```bash
   modprobe -r nvidia
   ```

3. Visning af, hvad der ville ske ved indlæsning af et modul uden at udføre det:
   ```bash
   modprobe -n nvidia
   ```

4. Indlæsning af et modul med detaljerede oplysninger:
   ```bash
   modprobe -v nvidia
   ```

## Tips
- Sørg for at have de nødvendige rettigheder (typisk root) for at indlæse eller fjerne moduler.
- Brug `modinfo [modulnavn]` for at få oplysninger om et specifikt modul, før du indlæser det.
- Vær opmærksom på afhængigheder mellem moduler; `modprobe` håndterer dem automatisk, men det er godt at være informeret.