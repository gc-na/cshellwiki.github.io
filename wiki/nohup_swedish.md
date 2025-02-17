# [Linux] Bash nohup användning: Kör kommandon utan att påverkas av utloggning

## Översikt
`nohup` (no hang up) är ett kommando i Unix-liknande operativsystem som tillåter användare att köra ett program eller skript i bakgrunden, vilket gör att det fortsätter att köras även om användaren loggar ut från systemet. Det är särskilt användbart för långvariga processer som inte ska avbrytas.

## Användning
Den grundläggande syntaxen för `nohup` är:

```bash
nohup [alternativ] [argument]
```

## Vanliga alternativ
- `&` - Kör kommandot i bakgrunden.
- `-h` - Visa hjälpmeddelande.
- `-v` - Visa versionsinformation.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nohup`:

1. **Köra ett skript i bakgrunden:**
   ```bash
   nohup ./mitt_skript.sh &
   ```

2. **Köra en långvarig process:**
   ```bash
   nohup python3 lång_process.py &
   ```

3. **Köra en kommando med utdata till en fil:**
   ```bash
   nohup ls -l > utdata.txt &
   ```

4. **Köra en process och ignorera utdata:**
   ```bash
   nohup my_command > /dev/null 2>&1 &
   ```

## Tips
- Använd `&` i slutet av kommandot för att säkerställa att det körs i bakgrunden.
- Kontrollera `nohup.out`-filen för att se utdata från kommandot om du inte har omdirigerat det.
- Tänk på att `nohup` inte skyddar mot systemavstängningar, så se till att spara ditt arbete innan du loggar ut.