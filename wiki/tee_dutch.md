# [Linux] C Shell (csh) tee gebruik: Schrijven naar bestanden en naar de standaarduitvoer

## Overzicht
De `tee`-opdracht in C Shell (csh) wordt gebruikt om de uitvoer van een commando naar meerdere bestemmingen te sturen. Het kan de uitvoer zowel naar de standaarduitvoer (meestal het scherm) als naar een of meer bestanden schrijven. Dit is handig wanneer je de uitvoer wilt bekijken en tegelijkertijd wilt opslaan.

## Gebruik
De basis syntaxis van de `tee`-opdracht is als volgt:

```csh
tee [opties] [bestanden]
```

## Veelvoorkomende opties
- `-a`: Voeg de uitvoer toe aan het einde van het opgegeven bestand in plaats van het bestand te overschrijven.
- `-i`: Negeer signalen, wat handig kan zijn om te voorkomen dat de opdracht voortijdig wordt beëindigd.

## Veelvoorkomende voorbeelden

1. **Basisgebruik van tee**:
   Dit voorbeeld toont hoe je de uitvoer van een commando naar een bestand schrijft en tegelijkertijd op het scherm weergeeft.
   ```csh
   echo "Hallo Wereld" | tee output.txt
   ```

2. **Uitvoer toevoegen aan een bestand**:
   Hier voegen we uitvoer toe aan een bestaand bestand zonder het te overschrijven.
   ```csh
   echo "Nieuwe regel" | tee -a output.txt
   ```

3. **Meerdere bestanden bijwerken**:
   Dit voorbeeld toont hoe je de uitvoer naar meerdere bestanden kunt sturen.
   ```csh
   echo "Dit is een test" | tee bestand1.txt bestand2.txt
   ```

4. **Gebruik met andere commando's**:
   Je kunt `tee` ook gebruiken in combinatie met andere commando's. Bijvoorbeeld, hier gebruiken we `ls` om de inhoud van een directory te tonen en tegelijkertijd naar een bestand te schrijven.
   ```csh
   ls -l | tee directory_list.txt
   ```

## Tips
- Gebruik de `-a` optie als je niet wilt dat je gegevens verloren gaan door het overschrijven van een bestand.
- Combineer `tee` met andere commando's in een pijplijn om de uitvoer te manipuleren en op te slaan.
- Vergeet niet dat `tee` de uitvoer naar de standaarduitvoer doorgeeft, dus je kunt de resultaten altijd in de terminal zien.