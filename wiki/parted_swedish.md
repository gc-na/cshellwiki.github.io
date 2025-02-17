# [Linux] Bash parted användning: Hantera partitioner på diskar

## Översikt
`parted` är ett kommandoradsverktyg som används för att hantera partitioner på hårddiskar. Det gör det möjligt att skapa, ta bort, ändra storlek på och hantera partitioner på ett effektivt sätt. `parted` stöder både MBR (Master Boot Record) och GPT (GUID Partition Table) partitioneringssystem.

## Användning
Den grundläggande syntaxen för `parted` är:

```bash
parted [alternativ] [argument]
```

## Vanliga alternativ
- `-s`, `--script`: Kör `parted` i skriptläge, vilket döljer interaktiva meddelanden.
- `-l`, `--list`: Lista alla tillgängliga diskar och deras partitioner.
- `mkpart`: Skapa en ny partition.
- `rm`: Ta bort en partition.
- `resizepart`: Ändra storlek på en befintlig partition.

## Vanliga exempel

### Lista partitioner
För att lista alla partitioner på systemets diskar kan du använda följande kommando:

```bash
parted -l
```

### Skapa en ny partition
För att skapa en ny partition på en disk, använd kommandot:

```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```
Detta skapar en primär partition av typen ext4 som sträcker sig från 1 MiB till 100 MiB på disken `/dev/sda`.

### Ta bort en partition
För att ta bort en specifik partition, använd:

```bash
parted /dev/sda rm 1
```
Detta tar bort partition 1 från disken `/dev/sda`.

### Ändra storlek på en partition
För att ändra storlek på en partition kan du använda följande kommando:

```bash
parted /dev/sda resizepart 1 200MiB
```
Detta ändrar storleken på partition 1 till 200 MiB.

## Tips
- Se alltid till att säkerhetskopiera viktiga data innan du gör ändringar på partitioner.
- Använd `-s` alternativet om du kör skript för att undvika interaktiva frågor.
- Kontrollera partitionernas nuvarande storlek och layout med `parted -l` innan du gör några ändringar.