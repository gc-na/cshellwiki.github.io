# [Linux] C Shell (csh) last: toon inloggeschiedenis

## Overzicht
De `last`-opdracht in C Shell toont de inloggeschiedenis van gebruikers op het systeem. Het geeft een lijst weer van de laatst ingelogde gebruikers, inclusief informatie over de tijd en de duur van hun sessies.

## Gebruik
De basis syntaxis van de `last`-opdracht is als volgt:

```csh
last [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n`: Beperk het aantal weergegeven inlogrecords tot het opgegeven aantal.
- `-R`: Toon geen hostnamen, alleen gebruikers en tijdstempels.
- `-f`: Specificeer een alternatieve wtmp-bestand om inloggegevens uit te lezen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `last`-opdracht:

1. Toon de laatste inlogrecords voor alle gebruikers:
   ```csh
   last
   ```

2. Toon de laatste 5 inlogrecords:
   ```csh
   last -n 5
   ```

3. Toon inlogrecords zonder hostnamen:
   ```csh
   last -R
   ```

4. Toon inlogrecords vanuit een specifiek wtmp-bestand:
   ```csh
   last -f /var/log/wtmp.1
   ```

## Tips
- Gebruik de `-n` optie om de uitvoer te beperken tot een beheersbaar aantal records, vooral op systemen met veel gebruikers.
- Combineer `last` met andere commando's zoals `grep` om specifieke gebruikers of tijdstippen te filteren.
- Controleer regelmatig de inloggeschiedenis om ongebruikelijke inlogpogingen of activiteiten te identificeren.