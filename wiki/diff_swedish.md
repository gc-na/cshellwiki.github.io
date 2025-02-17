# [Linux] Bash diff användning: Jämför filer och visa skillnader

## Översikt
`diff` är ett kommando som används för att jämföra innehållet i två filer rad för rad. Det visar skillnaderna mellan filerna, vilket gör det enkelt att se vad som har ändrats, lagts till eller tagits bort.

## Användning
Den grundläggande syntaxen för `diff` är:

```bash
diff [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-u`: Visar skillnaderna i ett sammanfattande format (unified format).
- `-c`: Visar skillnaderna i ett kontextformat.
- `-i`: Ignorerar skillnader i versaler.
- `-w`: Ignorerar alla vita tecken.
- `-r`: Jämför kataloger rekursivt.

## Vanliga exempel
Här är några praktiska exempel på hur `diff` kan användas:

1. Jämför två textfiler:
   ```bash
   diff fil1.txt fil2.txt
   ```

2. Visa skillnader i ett sammanfattande format:
   ```bash
   diff -u fil1.txt fil2.txt
   ```

3. Jämför två kataloger:
   ```bash
   diff -r katalog1/ katalog2/
   ```

4. Ignorera versaler när du jämför:
   ```bash
   diff -i fil1.txt fil2.txt
   ```

5. Visa skillnader med kontext:
   ```bash
   diff -c fil1.txt fil2.txt
   ```

## Tips
- Använd `-u` för att få en mer läsbar och sammanfattande visning av skillnaderna.
- När du arbetar med kataloger, använd `-r` för att se skillnader i alla filer inom katalogerna.
- För att spara skillnaderna till en fil kan du använda omdirigering:
  ```bash
  diff fil1.txt fil2.txt > skillnader.txt
  ```