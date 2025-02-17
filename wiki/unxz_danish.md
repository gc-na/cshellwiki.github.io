# [Linux] Bash unxz brug: Udpakning af .xz filer

## Oversigt
`unxz` er et kommandolinjeværktøj, der bruges til at dekomprimere filer, der er komprimeret med `xz`-formatet. Det fjerner komprimeringen og gendanner den originale fil.

## Brug
Den grundlæggende syntaks for `unxz`-kommandoen er:

```bash
unxz [muligheder] [argumenter]
```

## Almindelige muligheder
- `-k`, `--keep`: Behold den komprimerede fil efter dekomprimering.
- `-f`, `--force`: Tving dekomprimering, selvom der allerede findes en fil med samme navn.
- `-v`, `--verbose`: Vis detaljeret output under dekomprimeringsprocessen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `unxz`:

1. Dekomprimere en enkelt fil:
   ```bash
   unxz fil.xz
   ```

2. Dekomprimere en fil og beholde den originale:
   ```bash
   unxz -k fil.xz
   ```

3. Tvinge dekomprimering af en fil, selvom den originale allerede findes:
   ```bash
   unxz -f fil.xz
   ```

4. Dekomprimere flere filer på én gang:
   ```bash
   unxz fil1.xz fil2.xz fil3.xz
   ```

5. Vise detaljer under dekomprimering:
   ```bash
   unxz -v fil.xz
   ```

## Tips
- Sørg for at have en sikkerhedskopi af dine filer, inden du bruger `-f`-muligheden, da den kan overskrive eksisterende filer.
- Brug `-k`-muligheden, hvis du vil bevare de komprimerede filer til senere brug.
- Tjek filens integritet efter dekomprimering ved at sammenligne størrelsen eller indholdet af den originale og dekomprimerede fil.