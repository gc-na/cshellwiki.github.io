# [Linux] Bash resize2fs brug: Ændre størrelsen på filsystemer

## Oversigt
`resize2fs` er et værktøj, der bruges til at ændre størrelsen på ext2, ext3 og ext4 filsystemer. Det giver brugerne mulighed for at udvide eller reducere størrelsen på et filsystem, hvilket kan være nyttigt i mange situationer, såsom at optimere diskplads eller tilpasse filsystemet til ændrede databehov.

## Brug
Den grundlæggende syntaks for `resize2fs` er som følger:

```bash
resize2fs [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f` : Tvinger ændringen af størrelsen, selvom filsystemet er beskadiget.
- `-p` : Viser fremskridtet under ændringen af størrelsen.
- `-M` : Reducerer filsystemet til dets mindste størrelse.
- `-s` : Ændrer størrelsen på filsystemet til den angivne størrelse.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `resize2fs`:

1. **Udvidelse af et filsystem**:
   For at udvide et filsystem til at bruge al tilgængelig plads på partitionen, kan du bruge følgende kommando:
   ```bash
   resize2fs /dev/sda1
   ```

2. **Reducer størrelsen på et filsystem**:
   Hvis du vil reducere størrelsen på et filsystem til 20 GB, kan du bruge:
   ```bash
   resize2fs /dev/sda1 20G
   ```

3. **Tvinge ændring af størrelse**:
   Hvis du har brug for at tvinge ændringen af størrelsen på et beskadiget filsystem, kan du bruge:
   ```bash
   resize2fs -f /dev/sda1
   ```

4. **Vis fremskridt**:
   For at se fremskridtet, mens du ændrer størrelsen, kan du tilføje `-p`:
   ```bash
   resize2fs -p /dev/sda1
   ```

## Tips
- Sørg for at sikkerhedskopiere dine data, før du ændrer størrelsen på et filsystem, da der altid er en risiko for datatab.
- Det anbefales at køre `resize2fs` på et unmounted filsystem for at undgå problemer.
- Brug `df -h` til at kontrollere den nuværende størrelse og brug af filsystemet, før du foretager ændringer.