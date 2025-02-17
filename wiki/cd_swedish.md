# [Linux] Bash cd användning: Navigera i kataloger

## Översikt
Kommandot `cd` (change directory) används för att ändra den aktuella arbetskatalogen i terminalen. Det gör att användaren kan navigera mellan olika kataloger i filsystemet.

## Användning
Den grundläggande syntaxen för kommandot `cd` är:

```bash
cd [alternativ] [argument]
```

## Vanliga alternativ
- `-`: Byter till den senaste katalogen som användes.
- `..`: Går upp en nivå i katalogstrukturen.
- `~`: Går till användarens hemkatalog.

## Vanliga exempel
Här är några praktiska exempel på hur `cd` kan användas:

1. Gå till hemkatalogen:
   ```bash
   cd ~
   ```

2. Gå upp en nivå i katalogstrukturen:
   ```bash
   cd ..
   ```

3. Byta till en specifik katalog:
   ```bash
   cd /path/to/directory
   ```

4. Byta till den senaste använda katalogen:
   ```bash
   cd -
   ```

5. Gå till en katalog med mellanslag i namnet:
   ```bash
   cd "Mina Dokument"
   ```

## Tips
- Använd tab-tangenten för att automatiskt komplettera katalognamn, vilket sparar tid och minskar risken för fel.
- Kontrollera alltid din nuvarande katalog med kommandot `pwd` (print working directory) efter att du har använt `cd` för att bekräfta att du har navigerat till rätt plats.
- Om du ofta använder en specifik katalog kan du överväga att skapa en alias i din `.bashrc`-fil för snabbare åtkomst.