# [Linux] Bash watch brug: Opdatering af kommandouddata

## Oversigt
`watch`-kommandoen bruges til at køre en given kommando gentagne gange og vise dens output i realtid. Dette er nyttigt til overvågning af ændringer i outputtet af en kommando over tid, såsom systemstatus eller filændringer.

## Brug
Den grundlæggende syntaks for `watch`-kommandoen er:

```bash
watch [muligheder] [kommando]
```

## Almindelige muligheder
- `-n, --interval`: Angiver intervallet (i sekunder) mellem hver udførelse af kommandoen. Standardintervallet er 2 sekunder.
- `-d, --differences`: Marker ændringer i outputtet. Dette gør det lettere at se, hvad der er ændret mellem hver opdatering.
- `-t, --no-title`: Skjul overskriften, der viser kommandoen og tidsstemplet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `watch`:

1. **Overvågning af systemets hukommelsesbrug:**
   ```bash
   watch free -h
   ```

2. **Overvågning af diskplads:**
   ```bash
   watch df -h
   ```

3. **Overvågning af ændringer i en specifik fil:**
   ```bash
   watch -d cat /path/to/file.txt
   ```

4. **Kør en kommando hvert sekund:**
   ```bash
   watch -n 1 ls -l
   ```

## Tips
- Brug `-d` muligheden for at fremhæve ændringer i outputtet, hvilket kan være særligt nyttigt, når du overvåger systemressourcer.
- Juster intervallet med `-n` for at tilpasse, hvor ofte du vil have opdateringer, afhængigt af hvor hurtigt dataene ændrer sig.
- Overvej at bruge `-t` for at reducere visuel rod, hvis du kun er interesseret i outputtet og ikke i overskriften.