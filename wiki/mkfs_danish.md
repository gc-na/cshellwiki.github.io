# [Linux] Bash mkfs brug: Opret filsystemer på en enhed

## Oversigt
`mkfs` (make filesystem) er en Bash-kommando, der bruges til at oprette et filsystem på en lagringsenhed, såsom en harddisk eller USB-drev. Denne kommando formaterer en enhed og forbereder den til at gemme data.

## Brug
Den grundlæggende syntaks for `mkfs`-kommandoen er:

```bash
mkfs [muligheder] [argumenter]
```

## Almindelige muligheder
- `-t, --type`: Angiver typen af filsystem, der skal oprettes (f.eks. ext4, vfat).
- `-L, --label`: Tildeler et label til filsystemet.
- `-n, --no-progress`: Udelukker visning af fremdriftsinformation under formatet.
- `-V, --verbose`: Viser detaljerede oplysninger om, hvad der sker under oprettelsen af filsystemet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `mkfs`:

1. Oprette et ext4 filsystem på en enhed:
   ```bash
   mkfs.ext4 /dev/sdb1
   ```

2. Oprette et vfat filsystem med et specifikt label:
   ```bash
   mkfs.vfat -n "MinUSB" /dev/sdc1
   ```

3. Oprette et ext3 filsystem og vise detaljer om processen:
   ```bash
   mkfs.ext3 -V /dev/sdd1
   ```

4. Oprette et filsystem uden at vise fremdriftsinformation:
   ```bash
   mkfs.ext4 -n /dev/sde1
   ```

## Tips
- Sørg for at sikkerhedskopiere alle data på enheden, da `mkfs` vil slette eksisterende data.
- Tjek enhedens navn (f.eks. /dev/sdb1) ved hjælp af `lsblk`-kommandoen for at undgå at formatere den forkerte enhed.
- Overvej at bruge `-L` for at give dit filsystem et meningsfuldt navn, hvilket kan gøre det lettere at identificere senere.