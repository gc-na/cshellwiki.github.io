# [Linux] Bash hwclock brug: Håndterer hardwareklokken

## Oversigt
`hwclock` er et Bash-kommando, der bruges til at læse og opdatere hardwareklokken på en computer. Hardwareklokken er en uafhængig klokke, der holder styr på tiden, selv når systemet er slukket.

## Brug
Den grundlæggende syntaks for `hwclock`-kommandoen er:

```bash
hwclock [muligheder] [argumenter]
```

## Almindelige muligheder
- `--show`: Viser den nuværende tid fra hardwareklokken.
- `--set`: Sætter hardwareklokken til den angivne tid.
- `--hctosys`: Synkroniserer systemklokken med hardwareklokken.
- `--systohc`: Synkroniserer hardwareklokken med systemklokken.
- `--utc`: Angiver, at tiden skal behandles som UTC (Coordinated Universal Time).

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `hwclock`:

1. **Vis den nuværende tid fra hardwareklokken**:
   ```bash
   hwclock --show
   ```

2. **Synkroniser systemklokken med hardwareklokken**:
   ```bash
   hwclock --hctosys
   ```

3. **Synkroniser hardwareklokken med systemklokken**:
   ```bash
   hwclock --systohc
   ```

4. **Sæt hardwareklokken til en specifik tid**:
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

5. **Vis tid i UTC-format**:
   ```bash
   hwclock --show --utc
   ```

## Tips
- Sørg for at køre `hwclock` som superbruger (root) for at få de nødvendige tilladelser til at ændre hardwareklokken.
- Det er en god idé at synkronisere systemklokken og hardwareklokken regelmæssigt for at undgå tidsforskelle.
- Overvej at bruge `ntp` (Network Time Protocol) til automatisk tidsjustering, så hardwareklokken altid er præcis.