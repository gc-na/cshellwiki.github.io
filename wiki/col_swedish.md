# [Linux] Bash col användning: Rensar och formaterar textutdata

## Översikt
Kommandot `col` används för att rensa och formatera textutdata, särskilt för att ta bort backspaces och andra kontrolltecken. Det är användbart när man hanterar text som har formaterats för att skrivas ut, men som innehåller oönskade tecken.

## Användning
Den grundläggande syntaxen för `col` är:

```bash
col [alternativ] [argument]
```

## Vanliga alternativ
- `-b`: Tar bort backspaces.
- `-f`: Ignorerar formateringskommandon.
- `-x`: Använder en tabell med 8 tecken för tabbar.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `col`:

1. Rensa backspaces från en textfil:
   ```bash
   col -b < fil.txt > rensad_fil.txt
   ```

2. Formatera utdata från ett kommando och ta bort kontrolltecken:
   ```bash
   ls -l | col -b
   ```

3. Använda `col` för att rensa en fil och skriva ut resultatet direkt till terminalen:
   ```bash
   col < fil_med_kontrolltecken.txt
   ```

4. Ignorera formateringskommandon när man skriver ut en fil:
   ```bash
   col -f < fil_med_formatering.txt
   ```

## Tips
- Använd `col` i kombination med andra kommandon för att effektivt rensa och formatera utdata.
- Kontrollera alltid utdata efter att ha använt `col` för att säkerställa att det ser ut som förväntat.
- Experimentera med olika alternativ för att se vilken effekt de har på din textutdata.