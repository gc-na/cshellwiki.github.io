# [Linux] Bash nohup gebruik: Voorkom dat een proces stopt bij uitloggen

## Overzicht
De `nohup` (no hang up) opdracht in Bash wordt gebruikt om een proces uit te voeren dat niet wordt beëindigd wanneer de gebruiker zich afmeldt of de terminal sluit. Dit is bijzonder nuttig voor lange processen die je wilt laten draaien, zelfs als je niet meer ingelogd bent.

## Gebruik
De basis syntaxis van de `nohup` opdracht is als volgt:

```bash
nohup [opties] [argumenten]
```

## Veelvoorkomende opties
- `&` : Voegt het proces toe aan de achtergrond, zodat je de terminal kunt blijven gebruiken.
- `-o [bestand]` : Standaard uitvoer wordt naar het opgegeven bestand geschreven.
- `-h` : Toont de helpinformatie voor het gebruik van `nohup`.

## Veelvoorkomende voorbeelden

1. **Een script uitvoeren zonder dat het stopt bij uitloggen:**
   ```bash
   nohup ./mijn_script.sh &
   ```

2. **Een lange opdracht uitvoeren en de uitvoer naar een bestand schrijven:**
   ```bash
   nohup lange_opdracht > uitvoer.txt &
   ```

3. **Een Python-script uitvoeren in de achtergrond:**
   ```bash
   nohup python3 mijn_script.py &
   ```

4. **Een opdracht uitvoeren met foutmeldingen naar een apart bestand:**
   ```bash
   nohup mijn_opdracht > uitvoer.txt 2> fouten.txt &
   ```

## Tips
- Gebruik `&` om het proces in de achtergrond te laten draaien, zodat je de terminal kunt blijven gebruiken.
- Controleer regelmatig de uitvoerbestanden om te zien hoe je processen vorderen.
- Overweeg om `disown` te gebruiken na het starten van een `nohup` proces om het volledig los te koppelen van de terminal.