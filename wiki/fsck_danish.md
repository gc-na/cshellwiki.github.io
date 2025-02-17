# [Linux] Bash fsck brug: Kontroller og reparer filsystemer

## Oversigt
`fsck` (file system check) er et værktøj i Unix-lignende operativsystemer, der bruges til at kontrollere og reparere filsystemer. Det hjælper med at finde og rette fejl i filsystemet, hvilket er vigtigt for at sikre dataintegritet.

## Brug
Den grundlæggende syntaks for `fsck`-kommandoen er:

```bash
fsck [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Automatisk reparation af fejl uden at spørge brugeren.
- `-n`: Kør fsck i "read-only" mode, hvilket betyder, at ingen ændringer vil blive foretaget.
- `-y`: Svar automatisk "ja" på alle spørgsmål, der stilles under reparationen.
- `-t`: Angiv en timeout for operationen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `fsck`:

1. **Kontroller et specifikt filsystem**:
   ```bash
   fsck /dev/sda1
   ```

2. **Automatisk reparation af fejl**:
   ```bash
   fsck -a /dev/sda1
   ```

3. **Kør fsck i read-only mode**:
   ```bash
   fsck -n /dev/sda1
   ```

4. **Svar automatisk "ja" på alle spørgsmål**:
   ```bash
   fsck -y /dev/sda1
   ```

5. **Kontroller alle filsystemer i /etc/fstab**:
   ```bash
   fsck -A
   ```

## Tips
- Kør `fsck` kun på unmounted filsystemer for at undgå datatab.
- Det er en god idé at tage backup af vigtige data, før du kører reparationer.
- Brug `fsck` med forsigtighed, især med automatiske indstillinger som `-a` og `-y`, da de kan ændre filsystemet uden din bekræftelse.