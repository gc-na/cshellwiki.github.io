# [Linux] Bash ls gebruik: Lijst bestanden en mappen

## Overzicht
De `ls`-opdracht in Bash wordt gebruikt om de inhoud van een directory weer te geven. Het toont een lijst van bestanden en submappen in de opgegeven directory, wat handig is voor het navigeren door het bestandssysteem.

## Gebruik
De basis syntaxis van de `ls`-opdracht is als volgt:

```
ls [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelgebruikte opties voor de `ls`-opdracht:

- `-l`: Toont een gedetailleerde lijstweergave met informatie zoals bestandsrechten, eigenaar, grootte en datum van laatste wijziging.
- `-a`: Toont ook verborgen bestanden (bestanden die beginnen met een punt).
- `-h`: Toont bestandsgroottes in een leesbaar formaat (bijvoorbeeld KB, MB).
- `-R`: Toont de inhoud van subdirectories recursief.
- `-t`: Sorteert bestanden op tijd van laatste wijziging.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik**: Lijst de bestanden in de huidige directory.
   ```bash
   ls
   ```

2. **Lijst met details**: Toont een gedetailleerde lijst van bestanden.
   ```bash
   ls -l
   ```

3. **Verborgen bestanden weergeven**: Toont ook verborgen bestanden.
   ```bash
   ls -a
   ```

4. **Bestanden sorteren op tijd**: Toont bestanden gesorteerd op de datum van laatste wijziging.
   ```bash
   ls -lt
   ```

5. **Recursief weergeven**: Toont de inhoud van subdirectories.
   ```bash
   ls -R
   ```

## Tips
- Gebruik `ls -lh` om een overzicht te krijgen van bestanden met leesbare groottes.
- Combineer opties voor meer specifieke weergaven, bijvoorbeeld `ls -laR` om een gedetailleerd overzicht van alle bestanden in de huidige directory en subdirectories te krijgen.
- Vergeet niet dat de volgorde van opties niet uitmaakt; `ls -al` is hetzelfde als `ls -la`.