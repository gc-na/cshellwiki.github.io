# [Linux] Bash rmdir användning: Ta bort tomma kataloger

## Översikt
Kommandot `rmdir` används för att ta bort tomma kataloger i ett filsystem. Om katalogen innehåller filer eller andra kataloger kommer kommandot att misslyckas och ge ett felmeddelande.

## Användning
Den grundläggande syntaxen för kommandot är:

```
rmdir [alternativ] [argument]
```

## Vanliga alternativ
- `--ignore-fail-on-non-empty`: Ignorera fel om katalogen inte är tom.
- `--verbose`: Visa detaljerad information om vad som tas bort.
- `-p`: Ta bort kataloger och deras tomma överordnade kataloger.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `rmdir`:

1. Ta bort en tom katalog:
   ```bash
   rmdir minTomKatalog
   ```

2. Ta bort flera tomma kataloger:
   ```bash
   rmdir katalog1 katalog2 katalog3
   ```

3. Ta bort en tom underkatalog och dess tomma överordnade kataloger:
   ```bash
   rmdir -p minUnderKatalog/overordnadKatalog
   ```

4. Visa detaljerad information när du tar bort en katalog:
   ```bash
   rmdir --verbose minTomKatalog
   ```

## Tips
- Kontrollera alltid att katalogen är tom innan du använder `rmdir`, annars kommer kommandot att misslyckas.
- Använd alternativet `-p` för att effektivt ta bort flera tomma kataloger i en enda åtgärd.
- För att ta bort kataloger som inte är tomma, överväg att använda kommandot `rm -r` istället, men var försiktig, eftersom det tar bort allt innehåll i katalogen.