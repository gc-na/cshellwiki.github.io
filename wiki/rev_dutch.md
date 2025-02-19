# [Linux] C Shell (csh) rev: tekst omkeren

## Overzicht
De `rev`-opdracht in C Shell (csh) wordt gebruikt om de volgorde van de karakters in elke regel van een bestand of invoer om te keren. Dit kan nuttig zijn voor verschillende tekstverwerkingstaken.

## Gebruik
De basis syntaxis van de `rev`-opdracht is als volgt:

```
rev [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-` : Lees invoer van de standaardinvoer in plaats van een bestand.
- `-o [bestand]` : Schrijf de omgekeerde uitvoer naar het opgegeven bestand.

## Veelvoorkomende Voorbeelden

1. **Omgekeerde tekst van een bestand weergeven:**
   ```csh
   rev bestand.txt
   ```

2. **Omgekeerde tekst van standaardinvoer:**
   ```csh
   echo "Hallo Wereld" | rev
   ```

3. **Omgekeerde tekst naar een nieuw bestand schrijven:**
   ```csh
   rev bestand.txt -o omgekeerd.txt
   ```

4. **Meerdere bestanden omkeren:**
   ```csh
   rev bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik `rev` in combinatie met andere commando's via pijpen om complexe tekstverwerkingsopdrachten uit te voeren.
- Controleer altijd de uitvoer van `rev` met een klein voorbeeld voordat je het op grote bestanden toepast om onverwachte resultaten te voorkomen.