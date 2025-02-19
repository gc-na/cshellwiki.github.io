# [Linux] C Shell (csh) ls gebruik: Lijst bestanden en mappen

## Overzicht
De `ls`-opdracht in C Shell (csh) wordt gebruikt om de inhoud van een directory weer te geven. Het toont een lijst van bestanden en submappen, wat handig is voor het navigeren door de bestandssysteemstructuur.

## Gebruik
De basis syntaxis van de `ls`-opdracht is als volgt:

```csh
ls [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met de `ls`-opdracht:

- `-l`: Toont de bestanden in een lange lijstweergave, inclusief details zoals permissies, eigenaar, grootte en datum.
- `-a`: Toont ook verborgen bestanden (bestanden die beginnen met een punt).
- `-h`: Toont bestandsgroottes in een leesbaar formaat (bijv. K, M).
- `-R`: Toont de inhoud van submappen recursief.
- `-t`: Sorteert bestanden op tijd van laatste wijziging.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ls`-opdracht:

1. Gewone lijst van bestanden in de huidige directory:
   ```csh
   ls
   ```

2. Lijst van bestanden met details in lange weergave:
   ```csh
   ls -l
   ```

3. Lijst inclusief verborgen bestanden:
   ```csh
   ls -a
   ```

4. Lijst van bestanden met leesbare bestandsgroottes:
   ```csh
   ls -lh
   ```

5. Recursieve lijst van bestanden in de huidige directory en subdirectories:
   ```csh
   ls -R
   ```

6. Lijst van bestanden gesorteerd op tijd van laatste wijziging:
   ```csh
   ls -lt
   ```

## Tips
- Gebruik `ls -la` om een volledig overzicht van alle bestanden, inclusief verborgen bestanden, te krijgen.
- Combineer opties voor meer specifieke resultaten, zoals `ls -lhR` voor een gedetailleerde, leesbare, recursieve lijst.
- Vergeet niet dat de volgorde van opties niet uitmaakt; `ls -la` is hetzelfde als `ls -al`.