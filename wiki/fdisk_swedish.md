# [Linux] Bash fdisk användning: Hantera partitioner på diskar

## Översikt
`fdisk` är ett kraftfullt verktyg i Linux som används för att hantera partitioner på hårddiskar. Det gör det möjligt för användare att skapa, ta bort och ändra partitioner, vilket är avgörande för att organisera lagring på en dator.

## Användning
Den grundläggande syntaxen för `fdisk` är:

```bash
fdisk [alternativ] [enhet]
```

Där `[enhet]` vanligtvis är en enhet som `/dev/sda`, `/dev/sdb`, etc.

## Vanliga alternativ
- `-l`: Lista alla partitioner på alla enheter.
- `-u`: Använda sektorer istället för cylindrar för att visa partitioner.
- `-n`: Skapa en ny partition.
- `-d`: Ta bort en partition.
- `-t`: Ändra partitionstyp.

## Vanliga exempel

### Lista partitioner
För att lista alla partitioner på systemet kan du använda:

```bash
fdisk -l
```

### Skapa en ny partition
För att skapa en ny partition på `/dev/sda`, starta `fdisk` med enheten:

```bash
fdisk /dev/sda
```
Följ sedan instruktionerna för att skapa en ny partition.

### Ta bort en partition
För att ta bort en partition, använd:

```bash
fdisk /dev/sda
```
Välj alternativet för att ta bort partitionen och följ instruktionerna.

### Ändra partitionstyp
För att ändra typ på en partition, använd:

```bash
fdisk /dev/sda
```
Välj partitionen och ange den nya typkoden.

## Tips
- Var alltid försiktig när du använder `fdisk`, eftersom felaktiga ändringar kan leda till dataförlust.
- Gör alltid en säkerhetskopia av viktiga data innan du ändrar partitioner.
- Använd `man fdisk` för att läsa mer om kommandot och dess alternativ.