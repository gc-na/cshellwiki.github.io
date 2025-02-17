# [Linux] Bash lvm brug: Administrer logiske volumener

## Oversigt
`lvm` (Logical Volume Manager) er et værktøj til at administrere logiske volumener i Linux. Det giver brugerne mulighed for at oprette, ændre og slette logiske volumener, hvilket gør det lettere at håndtere diskplads og partitioner dynamisk.

## Brug
Den grundlæggende syntaks for `lvm`-kommandoen er som følger:

```bash
lvm [options] [arguments]
```

## Almindelige muligheder
- `create`: Opretter et nyt logisk volumen.
- `remove`: Sletter et eksisterende logisk volumen.
- `extend`: Udvider størrelsen på et logisk volumen.
- `reduce`: Reducerer størrelsen på et logisk volumen.
- `lvdisplay`: Viser information om logiske volumener.

## Almindelige eksempler

### Oprette et logisk volumen
For at oprette et logisk volumen kaldet `my_volume` på 10 GB i gruppen `my_volume_group`:
```bash
lvm lvcreate -n my_volume -L 10G my_volume_group
```

### Slette et logisk volumen
For at slette det logiske volumen `my_volume`:
```bash
lvm lvremove my_volume_group/my_volume
```

### Udvide et logisk volumen
For at udvide `my_volume` med 5 GB:
```bash
lvm lvextend -L +5G my_volume_group/my_volume
```

### Reducere et logisk volumen
For at reducere `my_volume` med 3 GB:
```bash
lvm lvreduce -L -3G my_volume_group/my_volume
```

### Vise information om logiske volumener
For at vise detaljer om alle logiske volumener:
```bash
lvm lvdisplay
```

## Tips
- Sørg for at tage backup af data, før du ændrer størrelsen på logiske volumener.
- Brug `lvdisplay` til at kontrollere status og information om volumener, før du udfører ændringer.
- Overvej at bruge `lvm` i scripts for at automatisere diskadministration.