# [Linux] Bash pushd användning: Navigera i kataloger

## Översikt
Kommandot `pushd` används för att ändra den aktuella katalogen och samtidigt spara den tidigare katalogen på en stack. Detta gör det enkelt att navigera fram och tillbaka mellan kataloger.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
pushd [alternativ] [argument]
```

## Vanliga alternativ
- `+n`: Gå till den n:te katalogen i stacken.
- `-n`: Gå tillbaka till den n:te katalogen i stacken.
- `-`: Byt till den senaste katalogen i stacken.

## Vanliga exempel
Här är några praktiska exempel på hur `pushd` kan användas:

1. **Navigera till en katalog och spara den nuvarande katalogen:**
   ```bash
   pushd /path/to/directory
   ```

2. **Återgå till den tidigare katalogen:**
   ```bash
   popd
   ```

3. **Navigera till den andra katalogen i stacken:**
   ```bash
   pushd +1
   ```

4. **Byt tillbaka till den senaste katalogen:**
   ```bash
   pushd -
   ```

## Tips
- Använd `dirs` för att visa katalogstacken och se var du befinner dig.
- Kombinera `pushd` och `popd` för att enkelt navigera mellan flera kataloger utan att behöva ange hela sökvägar.
- Tänk på att `pushd` kan användas i skript för att hantera kataloger effektivt, vilket gör skripten mer läsbara och lättare att underhålla.