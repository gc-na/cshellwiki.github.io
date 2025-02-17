# [Linux] Bash lvcreate brug: Opret logiske volumener

## Oversigt
`lvcreate` er et Bash-kommando, der bruges til at oprette logiske volumener i Linux Logical Volume Manager (LVM). Det giver brugerne mulighed for at administrere diskplads mere effektivt ved at opdele fysiske diske i logiske enheder.

## Brug
Den grundlæggende syntaks for `lvcreate` er som følger:

```bash
lvcreate [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n, --name <navn>`: Angiv navnet på det logiske volumen, der skal oprettes.
- `-L, --size <størrelse>`: Angiv størrelsen på det logiske volumen.
- `-l, --extents <antal>`: Angiv antallet af extents, der skal bruges til det logiske volumen.
- `-C, --mirrors <antal>`: Opret spejlvendte logiske volumener.
- `-Z, --zero n` : Angiv om det logiske volumen skal initialiseres med nuller.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `lvcreate`:

1. Opret et logisk volumen med navnet "data" på 10 GB:

   ```bash
   lvcreate -n data -L 10G vg01
   ```

2. Opret et logisk volumen med navnet "backup" på 5 extents:

   ```bash
   lvcreate -n backup -l 5 vg01
   ```

3. Opret et spejlvendt logisk volumen med navnet "mirror_data":

   ```bash
   lvcreate -n mirror_data -m 1 -L 20G vg01
   ```

4. Opret et logisk volumen og initialiser det med nuller:

   ```bash
   lvcreate -n new_volume -L 15G -Z y vg01
   ```

## Tips
- Sørg for at have tilstrækkelig plads i den fysiske volumen, før du opretter et logisk volumen.
- Brug `lvdisplay` for at se de eksisterende logiske volumener og deres egenskaber.
- Overvej at oprette snapshots af logiske volumener, hvis du har brug for at tage backup af data, inden du foretager ændringer.