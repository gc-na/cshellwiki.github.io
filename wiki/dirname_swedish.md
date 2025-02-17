# [Linux] Bash dirname användning: Hämta katalognamn från en sökväg

## Översikt
Kommandot `dirname` används för att extrahera katalognamnet från en given sökväg. Det returnerar den del av sökvägen som representerar katalogen, vilket kan vara användbart för skript och filhantering.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
dirname [alternativ] [argument]
```

## Vanliga alternativ
- `-z`: Behandlar tomma argument som en tom sträng.
- `--help`: Visar hjälpmeddelande för kommandot.
- `--version`: Visar versionsinformation för dirname.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `dirname`:

1. Hämta katalognamnet från en filväg:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Utdata:
   ```
   /home/user/documents
   ```

2. Använda dirname med en relativ sökväg:
   ```bash
   dirname ./folder/subfolder/file.txt
   ```
   Utdata:
   ```
   ./folder/subfolder
   ```

3. Hämta katalognamnet från en sökväg utan filnamn:
   ```bash
   dirname /var/log/
   ```
   Utdata:
   ```
   /var
   ```

4. Använda dirname i ett skript för att hämta katalogen där skriptet finns:
   ```bash
   DIR=$(dirname "$0")
   echo "Skriptets katalog är: $DIR"
   ```

## Tips
- Använd `dirname` i kombination med andra kommandon som `basename` för att få både katalog och filnamn.
- Var medveten om att `dirname` returnerar en tom sträng om den ges en tom sökväg.
- För bästa resultat, se till att ange fullständiga sökvägar för att undvika förvirring med relativa sökvägar.