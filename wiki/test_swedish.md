# [Linux] Bash test användning: Kontrollera villkor

## Översikt
Kommandot `test` används för att utvärdera villkor i Bash-skript och kommandorader. Det returnerar ett sanningsvärde (sant eller falskt) baserat på de angivna villkoren, vilket gör det användbart för att styra flödet i skript.

## Användning
Den grundläggande syntaxen för kommandot `test` är:

```bash
test [alternativ] [argument]
```

## Vanliga alternativ
- `-e fil`: Kontrollerar om filen existerar.
- `-d fil`: Kontrollerar om filen är en katalog.
- `-f fil`: Kontrollerar om filen är en vanlig fil.
- `-r fil`: Kontrollerar om filen är läsbar.
- `-w fil`: Kontrollerar om filen är skrivbar.
- `-x fil`: Kontrollerar om filen är körbar.
- `sträng1 = sträng2`: Kontrollerar om två strängar är lika.
- `sträng1 != sträng2`: Kontrollerar om två strängar inte är lika.
- `tal1 -eq tal2`: Kontrollerar om två tal är lika.
- `tal1 -ne tal2`: Kontrollerar om två tal inte är lika.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `test`:

1. Kontrollera om en fil existerar:
   ```bash
   test -e /path/to/file && echo "Filen finns."
   ```

2. Kontrollera om en katalog existerar:
   ```bash
   test -d /path/to/directory && echo "Katalogen finns."
   ```

3. Kontrollera om en fil är skrivbar:
   ```bash
   test -w /path/to/file && echo "Filen är skrivbar."
   ```

4. Jämföra två strängar:
   ```bash
   sträng1="hej"
   sträng2="hej"
   test "$sträng1" = "$sträng2" && echo "Strängarna är lika."
   ```

5. Jämföra två tal:
   ```bash
   tal1=5
   tal2=10
   test "$tal1" -lt "$tal2" && echo "$tal1 är mindre än $tal2."
   ```

## Tips
- Använd alltid citattecken runt variabler för att undvika problem med tomma eller specialtecken.
- Du kan använda `[` som en synonym för `test`, vilket kan göra kommandon mer läsbara. Exempel: `[ -e /path/to/file ]`.
- Kombinera flera villkor med `&&` (och) och `||` (eller) för mer komplex logik.