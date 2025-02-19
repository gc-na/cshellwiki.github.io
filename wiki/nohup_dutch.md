# [Linux] C Shell (csh) nohup gebruik: Voorkom dat een proces wordt beëindigd bij uitloggen

## Overzicht
De `nohup` (no hang up) opdracht in C Shell wordt gebruikt om een commando uit te voeren dat blijft draaien, zelfs nadat de gebruiker is uitgelogd. Dit is handig voor lange processen die niet moeten worden onderbroken.

## Gebruik
De basis syntaxis van de `nohup` opdracht is als volgt:

```
nohup [opties] [argumenten]
```

## Veelvoorkomende opties
- `&` : Voegt het proces toe aan de achtergrond, zodat je de terminal kunt blijven gebruiken.
- `-o [bestand]` : Specificeert een bestand waaruit de uitvoer van het proces wordt geschreven.
- `-h` : Geeft een helpbericht weer met informatie over het gebruik van de opdracht.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `nohup`:

1. Een script uitvoeren dat op de achtergrond draait:
   ```csh
   nohup ./mijn_script.sh &
   ```

2. Een lange opdracht uitvoeren en de uitvoer naar een bestand schrijven:
   ```csh
   nohup lange_opdracht > uitvoer.log &
   ```

3. Een Python-script uitvoeren zonder dat het wordt beëindigd bij uitloggen:
   ```csh
   nohup python3 mijn_script.py &
   ```

4. Een commando met een specifieke uitvoerbestand:
   ```csh
   nohup ls -l > lijst.txt &
   ```

## Tips
- Gebruik altijd `&` om het proces op de achtergrond te laten draaien, zodat je de terminal kunt blijven gebruiken.
- Controleer regelmatig het uitvoerbestand om de voortgang van je proces te volgen.
- Combineer `nohup` met `screen` of `tmux` voor extra controle over je processen.