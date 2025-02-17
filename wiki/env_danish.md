# [Linux] Bash env brug: Håndter miljøvariabler

## Oversigt
`env`-kommandoen bruges til at vise eller ændre miljøvariabler i et Unix-lignende operativsystem. Den kan også bruges til at køre et program med et ændret miljø.

## Brug
Den grundlæggende syntaks for `env`-kommandoen er:

```bash
env [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Start et nyt miljø uden eksisterende variabler.
- `-u`: Fjern en specifik miljøvariabel.
- `VAR=value`: Sæt en ny miljøvariabel for den pågældende kommando.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `env`:

1. **Vis alle miljøvariabler:**
   ```bash
   env
   ```

2. **Kør et program med et ændret miljø:**
   ```bash
   env VAR=value program
   ```

3. **Fjern en miljøvariabel:**
   ```bash
   env -u VAR program
   ```

4. **Start et program uden eksisterende miljøvariabler:**
   ```bash
   env -i program
   ```

## Tips
- Brug `env` til at teste, hvordan et program opfører sig uden bestemte miljøvariabler.
- Når du sætter miljøvariabler, skal du være opmærksom på, at de kun gælder for den pågældende kommando, medmindre du bruger `export` til at gøre dem permanente.
- `env` er nyttig i scripts, hvor du ønsker at sikre, at et program kører med et specifikt miljø.