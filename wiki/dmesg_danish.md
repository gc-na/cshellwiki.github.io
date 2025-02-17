# [Linux] Bash dmesg brug: Viser kernel-beskeder

## Oversigt
`dmesg` er et kommandolinjeværktøj, der bruges til at vise og kontrollere kernelens ringbuffer. Det viser meddelelser fra kerneprocessen, som kan være nyttige til fejlfinding af hardware- og driverproblemer.

## Brug
Den grundlæggende syntaks for `dmesg`-kommandoen er:

```bash
dmesg [options] [arguments]
```

## Almindelige muligheder
- `-C`: Rydder ringbufferen.
- `-c`: Rydder ringbufferen og viser de nuværende meddelelser.
- `-n level`: Sætter niveauet for meddelelser, der skal vises.
- `-T`: Viser tidsstempler i menneskeligt læsbart format.
- `--follow`: Følger nye meddelelser i realtid.

## Almindelige eksempler
1. **Vis alle kernelmeddelelser:**
   ```bash
   dmesg
   ```

2. **Vis meddelelser med tidsstempler:**
   ```bash
   dmesg -T
   ```

3. **Ryd ringbufferen og vis meddelelser:**
   ```bash
   dmesg -c
   ```

4. **Følg nye meddelelser i realtid:**
   ```bash
   dmesg --follow
   ```

5. **Vis kun meddelelser af en bestemt alvorlighed:**
   ```bash
   dmesg -n 3
   ```

## Tips
- Brug `dmesg -T` for at få en bedre forståelse af, hvornår meddelelserne blev genereret.
- Ryd ringbufferen med `-C` for at starte med en ren slate, hvis du vil fokusere på nye meddelelser.
- Kombiner `dmesg` med `grep` for at filtrere specifikke meddelelser, f.eks.:
  ```bash
  dmesg | grep error
  ```
- Vær opmærksom på, at `dmesg`-output kan være meget omfattende, så det kan være nyttigt at bruge `less` til at navigere i outputtet:
  ```bash
  dmesg | less
  ```