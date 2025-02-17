# [Linux] Bash fdisk brug: Partitionering af diske

## Oversigt
`fdisk` er et kommandolinjeværktøj, der bruges til at partitionere harddiske. Det giver brugerne mulighed for at oprette, slette, ændre og vise partitioner på en disk. `fdisk` er især nyttigt til at administrere partitioner på MBR (Master Boot Record) diske.

## Brug
Den grundlæggende syntaks for `fdisk` er:

```bash
fdisk [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Viser en liste over alle tilgængelige diske og deres partitioner.
- `-u`: Angiver, at størrelser skal vises i sektorer i stedet for cylinder.
- `-n`: Opretter en ny partition.
- `-d`: Sletter en eksisterende partition.
- `-t`: Ændrer partitionstypen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `fdisk` kan bruges:

1. **Liste over partitioner på en disk**:
   ```bash
   fdisk -l /dev/sda
   ```

2. **Oprette en ny partition**:
   Start `fdisk` med den ønskede disk:
   ```bash
   fdisk /dev/sda
   ```
   Følg derefter instruktionerne for at oprette en ny partition.

3. **Slette en partition**:
   Start `fdisk` med den ønskede disk:
   ```bash
   fdisk /dev/sda
   ```
   Brug kommandoen `d` til at slette en partition og følg instruktionerne.

4. **Ændre partitionstype**:
   Start `fdisk` med den ønskede disk:
   ```bash
   fdisk /dev/sda
   ```
   Brug kommandoen `t` for at ændre partitionstypen og angiv den ønskede type.

## Tips
- Sørg altid for at tage backup af vigtige data, inden du ændrer partitioner.
- Brug `man fdisk` for at få adgang til den fulde manual og lære om flere muligheder og funktioner.
- Vær forsigtig med at vælge den rigtige disk og partition, da forkert brug kan føre til datatab.