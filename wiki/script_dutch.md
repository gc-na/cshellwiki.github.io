# [Linux] C Shell (csh) script gebruik: Maak een opname van de terminalsessie

## Overzicht
De `script` opdracht in C Shell (csh) wordt gebruikt om een opname van een terminalsessie te maken. Dit is handig voor het vastleggen van de uitvoer van commando's en interacties in de terminal, zodat je deze later kunt bekijken of delen.

## Gebruik
De basis syntaxis van de `script` opdracht is als volgt:

```
script [opties] [bestandsnaam]
```

## Veelvoorkomende Opties
- `-a`: Voeg de uitvoer toe aan een bestaand bestand in plaats van het te overschrijven.
- `-q`: Voer de opdracht uit in stille modus, zonder melding van het starten of stoppen van de opname.
- `-t`: Registreer de tijdstempels van de sessie in een aparte timing-bestand.

## Veelvoorkomende Voorbeelden

1. **Basis opname starten**
   ```csh
   script sessie.txt
   ```
   Dit commando start een nieuwe sessie en slaat de uitvoer op in `sessie.txt`.

2. **Opname in stille modus**
   ```csh
   script -q sessie_stil.txt
   ```
   Dit start een opname zonder meldingen, en slaat de uitvoer op in `sessie_stil.txt`.

3. **Bestaande opname aanvullen**
   ```csh
   script -a sessie_bestaand.txt
   ```
   Dit voegt nieuwe uitvoer toe aan `sessie_bestaand.txt` in plaats van het te overschrijven.

4. **Tijdstempels registreren**
   ```csh
   script -t sessie_tijd.txt
   ```
   Dit registreert de uitvoer in `sessie_tijd.txt` en houdt ook de tijdstempels bij in een apart bestand.

## Tips
- Zorg ervoor dat je de opname beëindigt met het commando `exit` of door de terminal te sluiten om de sessie correct op te slaan.
- Controleer de inhoud van het opnamebestand na afloop om te bevestigen dat alles correct is vastgelegd.
- Gebruik de `-a` optie als je meerdere sessies wilt combineren in één bestand voor een beter overzicht.