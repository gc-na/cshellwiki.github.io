# [Linux] Bash uniq Bruk: Fjerner duplikater fra sorterte linjer

## Oversikt
`uniq`-kommandoen brukes til å fjerne dupliserte linjer fra en sortert fil eller standard input. Den viser bare unike linjer, noe som gjør den nyttig for å rydde opp i data.

## Bruk
Grunnleggende syntaks for `uniq`-kommandoen er som følger:

```bash
uniq [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Teller antall forekomster av hver linje.
- `-d`: Viser bare linjer som er duplikater.
- `-u`: Viser bare linjer som er unike.
- `-i`: Ignorerer store og små bokstaver ved sammenligning.

## Vanlige eksempler

1. **Fjerne duplikater fra en fil:**
   Hvis du har en fil kalt `data.txt` med dupliserte linjer, kan du bruke:
   ```bash
   uniq data.txt
   ```

2. **Telle antall forekomster av hver linje:**
   For å se hvor mange ganger hver linje forekommer, kan du bruke:
   ```bash
   uniq -c data.txt
   ```

3. **Vise bare duplikater:**
   For å vise linjer som har duplikater, kan du bruke:
   ```bash
   uniq -d data.txt
   ```

4. **Vise bare unike linjer:**
   For å vise linjer som ikke har duplikater, kan du bruke:
   ```bash
   uniq -u data.txt
   ```

5. **Bruke med sortering:**
   Ofte må du sortere filen før du bruker `uniq`. Du kan gjøre dette i én linje:
   ```bash
   sort data.txt | uniq
   ```

## Tips
- Sørg for at dataene dine er sortert før du bruker `uniq`, ellers vil ikke duplikater bli fjernet riktig.
- Kombiner `uniq` med andre kommandoer som `sort` for mer effektive databehandlingstrinn.
- Bruk `-i` for å gjøre sammenligningen mer fleksibel, spesielt når du arbeider med tekst som kan ha varierende bokstavstørrelse.