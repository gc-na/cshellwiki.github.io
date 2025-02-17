# [Linux] Bash lsmod brug: Viser indlæste moduler i kerne

## Oversigt
`lsmod` er et Bash-kommando, der bruges til at vise de indlæste moduler i Linux-kernen. Det giver en liste over alle de moduler, der aktuelt er aktive i systemet, hvilket kan være nyttigt til fejlfinding og systemadministration.

## Brug
Den grundlæggende syntaks for `lsmod` er som følger:

```bash
lsmod [options] [arguments]
```

## Almindelige muligheder
`lsmod` har ikke mange muligheder, men her er nogle af de mest almindelige:

- **-h, --help**: Viser hjælp og information om brugen af kommandoen.
- **-v, --version**: Viser versionsoplysninger om `lsmod`.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `lsmod`:

1. **Vis alle indlæste moduler**:
   ```bash
   lsmod
   ```

2. **Vis hjælp til lsmod**:
   ```bash
   lsmod --help
   ```

3. **Vis versionsoplysninger**:
   ```bash
   lsmod --version
   ```

## Tips
- Brug `lsmod` sammen med `grep` for at filtrere resultaterne. For eksempel, hvis du vil finde et specifikt modul:
  ```bash
  lsmod | grep modulnavn
  ```

- Det kan være nyttigt at kombinere `lsmod` med `modinfo` for at få mere information om et bestemt modul:
  ```bash
  modinfo modulnavn
  ```

- Husk, at `lsmod` kun viser moduler, der er indlæst i den nuværende kerne. Hvis du har brug for at indlæse eller fjerne moduler, skal du bruge `modprobe` eller `rmmod`.