# [Linux] Bash parted brug: Administrer partitioner på disk

## Oversigt
`parted` er et kommandolinjeværktøj, der bruges til at oprette, slette og ændre partitioner på harddiske. Det giver brugerne mulighed for at håndtere partitioner effektivt og understøtter både MBR og GPT partitioneringsskemaer.

## Brug
Den grundlæggende syntaks for `parted`-kommandoen er:

```bash
parted [options] [arguments]
```

## Almindelige muligheder
- `-l`, `--list`: Vis en liste over alle tilgængelige diske og deres partitioner.
- `mklabel`: Opret en ny partitioneringsskabelon (f.eks. gpt eller msdos).
- `mkpart`: Opret en ny partition.
- `rm`: Slet en eksisterende partition.
- `resizepart`: Ændre størrelsen på en eksisterende partition.
- `print`: Vis partitionstabel for den valgte disk.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `parted` kan bruges:

### Liste over diske
For at vise en liste over alle tilgængelige diske og deres partitioner, kan du bruge:

```bash
parted -l
```

### Oprette en ny partition
For at oprette en ny partition på en disk, kan du bruge følgende kommando:

```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Slette en partition
For at slette partition nummer 2 på en disk, kan du bruge:

```bash
parted /dev/sda rm 2
```

### Ændre størrelsen på en partition
For at ændre størrelsen på partition 1 til at fylde op til 200MiB, kan du bruge:

```bash
parted /dev/sda resizepart 1 200MiB
```

### Vise partitionstabel
For at vise partitionstabellen for en disk, kan du bruge:

```bash
parted /dev/sda print
```

## Tips
- Sørg altid for at tage backup af dine data, før du ændrer partitioner.
- Brug `parted` med forsigtighed, da forkert brug kan føre til datatab.
- Kør `parted` som superbruger (root) for at få de nødvendige rettigheder til at ændre partitioner.