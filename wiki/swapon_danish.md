# [Linux] Bash swapon brug: Aktivér swap-plads

## Oversigt
`swapon`-kommandoen bruges til at aktivere swap-plads på et Linux-system. Swap-plads er en del af harddisken, der bruges som virtuel hukommelse, når den fysiske RAM er fuld. Ved at aktivere swap kan systemet håndtere flere processer uden at løbe tør for hukommelse.

## Brug
Den grundlæggende syntaks for `swapon`-kommandoen er:

```bash
swapon [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Aktiverer alle swap-enheder, der er angivet i `/etc/fstab`.
- `-s`: Viser en oversigt over de aktive swap-enheder.
- `--show`: Viser detaljerede oplysninger om de aktive swap-enheder.

## Almindelige eksempler

Aktiver en specifik swap-fil:
```bash
sudo swapon /path/to/swapfile
```

Aktiver alle swap-enheder fra `/etc/fstab`:
```bash
sudo swapon -a
```

Vis aktive swap-enheder:
```bash
swapon --show
```

## Tips
- Sørg for, at swap-filen eller partitionen er oprettet korrekt, før du aktiverer den.
- Brug `free -h` til at kontrollere hukommelses- og swap-brug efter aktivering.
- Deaktiver swap med `swapoff`-kommandoen, hvis du ikke længere har brug for det.