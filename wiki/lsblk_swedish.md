# [Linux] Bash lsblk användning: Visa blockenheter

## Översikt
`lsblk` är ett kommandoradsverktyg i Linux som används för att visa information om blockenheter, såsom hårddiskar och partitioner. Det ger en översikt över systemets lagringsenheter och deras hierarki.

## Användning
Den grundläggande syntaxen för `lsblk` är:

```bash
lsblk [alternativ] [argument]
```

## Vanliga alternativ
- `-a`, `--all`: Visa alla blockenheter, inklusive tomma.
- `-f`, `--fs`: Visa filsysteminformation för varje enhet.
- `-l`, `--list`: Visa enheter i en lista istället för en trädstruktur.
- `-o`, `--output`: Specifika kolumner att visa, t.ex. `NAME,SIZE,TYPE`.
- `-p`, `--paths`: Visa enhetsvägar istället för enhetsnamn.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `lsblk`:

### Visa alla blockenheter
```bash
lsblk
```

### Visa alla blockenheter inklusive tomma
```bash
lsblk -a
```

### Visa filsysteminformation
```bash
lsblk -f
```

### Visa enheter i lista
```bash
lsblk -l
```

### Visa specifika kolumner
```bash
lsblk -o NAME,SIZE,TYPE
```

## Tips
- Använd `lsblk -f` för att snabbt se vilket filsystem som används på varje enhet.
- Kombinera `lsblk` med andra kommandon som `grep` för att filtrera specifika enheter.
- Använd `man lsblk` för att läsa mer om alla tillgängliga alternativ och detaljerad information om kommandot.