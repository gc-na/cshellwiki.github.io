# [Linux] Bash fmt användning: Formatera text

## Översikt
Kommandot `fmt` används för att formatera textfiler genom att justera radlängden och göra texten mer läsbar. Det är särskilt användbart för att styra hur text visas i terminalen eller i utskrifter.

## Användning
Den grundläggande syntaxen för kommandot `fmt` är:

```bash
fmt [alternativ] [argument]
```

## Vanliga alternativ
- `-w, --width`: Anger den maximala radlängden. Standardvärdet är 75 tecken.
- `-s, --split-only`: Dela endast rader som redan är längre än den angivna bredden.
- `-u, --uniform`: Gör texten mer enhetlig genom att justera avståndet mellan ord.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `fmt`:

1. **Formatera en textfil till standardbredd**:
   ```bash
   fmt fil.txt
   ```

2. **Formatera en textfil med en specifik radlängd**:
   ```bash
   fmt -w 50 fil.txt
   ```

3. **Dela endast långa rader**:
   ```bash
   fmt -s fil.txt
   ```

4. **Använda uniform formatering**:
   ```bash
   fmt -u fil.txt
   ```

## Tips
- Använd `cat` i kombination med `fmt` för att snabbt formatera text från standardinmatning:
  ```bash
  cat fil.txt | fmt
  ```
- Om du vill spara den formaterade texten till en ny fil kan du använda omdirigering:
  ```bash
  fmt fil.txt > formaterad_fil.txt
  ```
- Tänk på att `fmt` inte ändrar originalfilen; det skapar en ny utdata. Använd omdirigering för att spara ändringar om det behövs.