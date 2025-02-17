# [Linux] Bash nl användning: Numrera rader i en fil

## Översikt
Kommandot `nl` används för att numrera rader i en textfil. Det är ett enkelt verktyg som gör det lättare att referera till specifika rader i en fil genom att lägga till radnummer.

## Användning
Den grundläggande syntaxen för `nl` är:

```
nl [alternativ] [argument]
```

## Vanliga alternativ
- `-b` : Anger vilken typ av radnummer som ska användas. Till exempel, `-b a` numrerar alla rader.
- `-f` : Anger hur många rader som ska hoppa över i början av filen.
- `-n` : Anger formatet för radnumreringen. Till exempel, `-n ln` för att numrera rader med ledande nollor.
- `-w` : Anger bredden på radnumret.
- `-s` : Anger en sträng som ska användas som separator mellan radnumret och innehållet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nl`:

1. Numrera alla rader i en fil:
   ```bash
   nl fil.txt
   ```

2. Numrera rader med en specifik separator:
   ```bash
   nl -s ": " fil.txt
   ```

3. Hoppa över de första 2 raderna innan numrering:
   ```bash
   nl -f 2 fil.txt
   ```

4. Använda ledande nollor för radnumrering:
   ```bash
   nl -n ln -w 3 fil.txt
   ```

5. Numrera endast icke-tomma rader:
   ```bash
   nl -b t fil.txt
   ```

## Tips
- Använd `nl` tillsammans med andra kommandon, som `cat`, för att visa numrerade rader direkt i terminalen.
- Experimentera med olika alternativ för att anpassa utseendet på numreringen efter dina behov.
- Kom ihåg att `nl` inte ändrar originalfilen; det skriver ut resultatet till standardutgången. Om du vill spara det numrerade resultatet kan du använda omdirigering.