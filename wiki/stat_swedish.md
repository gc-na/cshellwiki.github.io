# [Linux] Bash stat användning: Visa filinformation

## Översikt
Kommandot `stat` används för att visa detaljerad information om filer och kataloger i ett filsystem. Det ger användaren en översikt över filens attribut, såsom storlek, behörigheter, ägare och tidsstämplar.

## Användning
Den grundläggande syntaxen för kommandot `stat` är:

```bash
stat [alternativ] [argument]
```

## Vanliga alternativ
- `-c` : Anpassa utdataformatet med en specifik formatsträng.
- `-f` : Visa information om filsystemet istället för filen.
- `--help` : Visa hjälpmeddelande för kommandot.
- `--version` : Visa versionsinformation för `stat`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `stat`:

1. Visa information om en specifik fil:
   ```bash
   stat fil.txt
   ```

2. Visa information om en katalog:
   ```bash
   stat /home/användare
   ```

3. Anpassa utdataformatet för att visa endast filens storlek och senaste ändringstid:
   ```bash
   stat -c "Storlek: %s bytes, Ändrad: %y" fil.txt
   ```

4. Visa information om filsystemet där en fil ligger:
   ```bash
   stat -f fil.txt
   ```

## Tips
- Använd `--help` för att snabbt få en översikt över tillgängliga alternativ och deras funktioner.
- För att enkelt spara utdata från `stat` till en fil, kan du använda omdirigering:
  ```bash
  stat fil.txt > fil_info.txt
  ```
- Experimentera med formatsträngar i `-c` alternativet för att få utdata i det format du behöver för skript eller rapporter.