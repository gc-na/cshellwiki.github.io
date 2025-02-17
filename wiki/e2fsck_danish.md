# [Linux] Bash e2fsck brug: Kontrol af filsystemintegritet

## Oversigt
e2fsck er et værktøj, der bruges til at kontrollere og reparere filsystemer, der er baseret på ext2, ext3 eller ext4. Det hjælper med at sikre, at filsystemet er i en sund tilstand og kan forhindre datatab ved at identificere og rette fejl.

## Brug
Den grundlæggende syntaks for e2fsck-kommandoen er som følger:

```bash
e2fsck [muligheder] [argumenter]
```

## Almindelige muligheder
- `-p`: Udfør en hurtig kontrol og reparation af filsystemet uden at spørge brugeren.
- `-f`: Tvinge kontrol af filsystemet, selvom det ser ud til at være sundt.
- `-n`: Udfør kontrol uden at ændre noget; nyttigt til diagnosticering.
- `-y`: Svar ja til alle forespørgsler, så reparationer udføres automatisk.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger e2fsck:

1. **Kontroller et filsystem uden at ændre noget:**
   ```bash
   e2fsck -n /dev/sda1
   ```

2. **Udfør en hurtig kontrol og reparation:**
   ```bash
   e2fsck -p /dev/sda1
   ```

3. **Tving kontrol af et filsystem:**
   ```bash
   e2fsck -f /dev/sda1
   ```

4. **Reparer et filsystem automatisk uden at spørge:**
   ```bash
   e2fsck -y /dev/sda1
   ```

## Tips
- Sørg for at unmount filsystemet, før du kører e2fsck for at undgå datakorruption.
- Kør e2fsck regelmæssigt som en del af vedligeholdelsen af dit system for at sikre filsystemets integritet.
- Brug `-n` muligheden først for at se, hvilke problemer der kan være, før du foretager reparationer.