# [Linux] Bash env Bruk: Håndtere miljøvariabler

## Oversikt
`env`-kommandoen brukes til å vise eller endre miljøvariabler i Bash. Den kan også brukes til å kjøre et program med et modifisert miljø, noe som gjør den nyttig for testing og utvikling.

## Bruk
Den grunnleggende syntaksen for `env`-kommandoen er:

```bash
env [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-i`: Start et nytt miljø med ingen eksisterende variabler.
- `-u VARIABEL`: Fjern en spesifisert variabel fra miljøet.
- `VARIABEL=verdi`: Sett en variabel til en spesifisert verdi før du kjører et program.

## Vanlige Eksempler

1. **Vis alle miljøvariabler:**

   ```bash
   env
   ```

2. **Kjør et program med et spesifikt miljø:**

   ```bash
   env VARIABEL=verdi programnavn
   ```

3. **Fjern en variabel fra miljøet:**

   ```bash
   env -u VARIABEL programnavn
   ```

4. **Start et program med et rent miljø:**

   ```bash
   env -i programnavn
   ```

## Tips
- Bruk `env` for å teste hvordan et program oppfører seg uten eksisterende miljøvariabler.
- Når du setter miljøvariabler, husk at de kun gjelder for den spesifikke kommandoen som kjøres etter `env`.
- For å se spesifikke variabler, kan du kombinere `env` med `grep`:

   ```bash
   env | grep VARIABEL
   ```