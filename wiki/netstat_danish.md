# [Linux] Bash netstat brug: Vise netværksforbindelser

## Oversigt
`netstat` er et kommandolinjeværktøj, der bruges til at vise netværksforbindelser, routing-tabeller, interface-statistik og meget mere. Det er nyttigt til fejlfinding af netværksproblemer og overvågning af netværksaktivitet.

## Brug
Den grundlæggende syntaks for `netstat`-kommandoen er:

```bash
netstat [options] [arguments]
```

## Almindelige muligheder
- `-a`: Viser alle forbindelser og lytteporte.
- `-t`: Viser TCP-forbindelser.
- `-u`: Viser UDP-forbindelser.
- `-n`: Viser adresser og portnumre i numerisk format.
- `-l`: Viser kun lytteporte.
- `-p`: Viser PID og programnavn, der ejer forbindelsen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `netstat`:

1. **Vis alle aktive forbindelser:**
   ```bash
   netstat -a
   ```

2. **Vis kun TCP-forbindelser:**
   ```bash
   netstat -t
   ```

3. **Vis lytteporte:**
   ```bash
   netstat -l
   ```

4. **Vis forbindelser med numeriske adresser:**
   ```bash
   netstat -n
   ```

5. **Vis alle forbindelser med PID og programnavn:**
   ```bash
   netstat -p
   ```

## Tips
- Brug `netstat -tuln` for at få en hurtig oversigt over alle lytte-TCP og UDP-porte med numeriske adresser.
- Kombiner flere muligheder for at få mere detaljerede oplysninger, f.eks. `netstat -tulpan` for at se alle lytteporte med programnavne.
- Overvej at bruge `ss`-kommandoen som et alternativ til `netstat`, da den kan give mere detaljerede oplysninger og er hurtigere.