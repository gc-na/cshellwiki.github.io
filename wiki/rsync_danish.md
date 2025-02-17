# [Linux] Bash rsync brug: Synkronisering af filer og mapper

## Overview
`rsync` er et kraftfuldt værktøj til at synkronisere filer og mapper mellem to placeringer, enten lokalt eller over et netværk. Det er effektivt, fordi det kun overfører de ændrede dele af filer, hvilket sparer båndbredde og tid.

## Usage
Den grundlæggende syntaks for `rsync` er:

```bash
rsync [options] [source] [destination]
```

## Common Options
Her er nogle almindelige muligheder for `rsync`:

- `-a`: Arkivtilstand; bevarer filrettigheder, tidsstempler og symlinks.
- `-v`: Verbose; viser detaljer om, hvad der bliver overført.
- `-z`: Komprimering; komprimerer data under overførsel for at spare båndbredde.
- `-r`: Rekursiv; kopierer mapper og deres indhold.
- `--delete`: Sletter filer i destinationen, som ikke findes i kilden.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `rsync`:

1. **Kopier en lokal mappe til en anden lokal mappe:**

   ```bash
   rsync -av /sti/til/kilde/ /sti/til/destination/
   ```

2. **Kopier filer fra en lokal mappe til en fjernserver:**

   ```bash
   rsync -avz /sti/til/kilde/ bruger@server:/sti/til/destination/
   ```

3. **Kopier filer fra en fjernserver til en lokal mappe:**

   ```bash
   rsync -avz bruger@server:/sti/til/kilde/ /sti/til/destination/
   ```

4. **Brug `--delete` for at synkronisere og fjerne uønskede filer:**

   ```bash
   rsync -av --delete /sti/til/kilde/ /sti/til/destination/
   ```

## Tips
- Brug `-n` eller `--dry-run` for at se, hvad der ville blive overført, uden faktisk at udføre overførslen.
- Overvej at bruge `-e ssh` for at sikre, at overførslen til en fjernserver er krypteret.
- Planlæg regelmæssige synkroniseringer ved hjælp af cron-jobs for at holde dine data opdaterede.