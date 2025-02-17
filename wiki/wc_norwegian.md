# [Linux] Bash wc Bruk: Telle linjer, ord og tegn i filer

## Oversikt
`wc` (word count) er en Bash-kommando som brukes til å telle linjer, ord og tegn i en fil eller fra standard input. Den gir en enkel måte å få statistikk om innholdet i tekstfiler.

## Bruk
Grunnleggende syntaks for `wc`-kommandoen er som følger:

```bash
wc [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: Teller antall linjer.
- `-w`: Teller antall ord.
- `-c`: Teller antall tegn.
- `-m`: Teller antall tegn (inkludert multibyte-tegn).
- `-L`: Viser lengden på den lengste linjen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `wc` kan brukes:

1. **Telle linjer i en fil:**
   ```bash
   wc -l filnavn.txt
   ```

2. **Telle ord i en fil:**
   ```bash
   wc -w filnavn.txt
   ```

3. **Telle tegn i en fil:**
   ```bash
   wc -c filnavn.txt
   ```

4. **Bruke `wc` med pipelining for å telle ord fra en kommando:**
   ```bash
   echo "Hei verden" | wc -w
   ```

5. **Telle lengden på den lengste linjen i en fil:**
   ```bash
   wc -L filnavn.txt
   ```

## Tips
- Du kan kombinere alternativer for å få flere tellinger samtidig. For eksempel:
  ```bash
  wc -l -w filnavn.txt
  ```
- For å telle ord i flere filer samtidig, kan du spesifisere flere filnavn:
  ```bash
  wc -w fil1.txt fil2.txt
  ```
- Bruk `wc` sammen med andre kommandoer for mer avansert tekstbehandling, som å filtrere ut spesifikke linjer før telling.