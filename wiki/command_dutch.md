# [Linux] Bash command gebruik: [bestanden en mappen beheren]

## Overzicht
De `ls`-opdracht wordt gebruikt om de inhoud van een directory weer te geven. Het toont bestanden en mappen in de huidige of opgegeven directory, waardoor gebruikers snel kunnen zien wat er beschikbaar is.

## Gebruik
De basis syntaxis van de `ls`-opdracht is als volgt:

```
ls [opties] [bestanden]
```

## Veelvoorkomende opties
- `-l`: Toon de inhoud in een lange lijstvorm, inclusief details zoals permissies, eigenaar, grootte en datum.
- `-a`: Toon ook verborgen bestanden (bestanden die beginnen met een punt).
- `-h`: Toon bestandsgroottes in een leesbaar formaat (bijv. KB, MB).
- `-R`: Toon de inhoud van directories recursief.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ls`-opdracht:

1. Toon de inhoud van de huidige directory:
   ```bash
   ls
   ```

2. Toon de inhoud met details:
   ```bash
   ls -l
   ```

3. Toon ook verborgen bestanden:
   ```bash
   ls -a
   ```

4. Toon de inhoud met leesbare bestandsgroottes:
   ```bash
   ls -lh
   ```

5. Toon de inhoud van een specifieke directory:
   ```bash
   ls /pad/naar/directory
   ```

6. Toon de inhoud van directories recursief:
   ```bash
   ls -R
   ```

## Tips
- Combineer opties voor meer gedetailleerde weergave, bijvoorbeeld `ls -la` om zowel verborgen bestanden als details te tonen.
- Gebruik de tab-toets om automatisch bestandsnamen in te vullen, wat tijd bespaart en typfouten voorkomt.
- Overweeg om de alias `ll` in te stellen om `ls -l` snel te kunnen uitvoeren.