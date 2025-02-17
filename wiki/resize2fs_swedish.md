# [Linux] Bash resize2fs användning: Ändra storlek på ext2/ext3/ext4 filsystem

## Översikt
Kommandot `resize2fs` används för att ändra storlek på ext2, ext3 och ext4 filsystem. Det kan både öka och minska storleken på ett filsystem, vilket är användbart när du behöver justera lagringsutrymmet på en partition.

## Användning
Den grundläggande syntaxen för `resize2fs` är:

```bash
resize2fs [alternativ] [argument]
```

## Vanliga alternativ
- `-f`: Tvinga en storleksändring även om filsystemet verkar vara i ett ogiltigt tillstånd.
- `-p`: Visa framsteg under processen.
- `-s`: Minska storleken på filsystemet till den angivna storleken.
- `-M`: Minska filsystemet till den minsta storleken som är möjlig.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `resize2fs`:

### Öka storleken på ett filsystem
För att öka storleken på ett filsystem till att fylla hela partitionen kan du använda följande kommando:

```bash
resize2fs /dev/sda1
```

### Minska storleken på ett filsystem
För att minska storleken på ett filsystem till 20 GB:

```bash
resize2fs -s 20G /dev/sda1
```

### Visa framsteg under storleksändring
Om du vill se framstegen när du ändrar storlek på filsystemet:

```bash
resize2fs -p /dev/sda1
```

## Tips
- Se alltid till att säkerhetskopiera viktiga data innan du ändrar storleken på ett filsystem, särskilt när du minskar storleken.
- Använd `df -h` för att kontrollera filsystemets nuvarande storlek och användning innan du utför `resize2fs`.
- Det är bäst att avmontera filsystemet innan du ändrar storlek på det för att undvika dataförlust.