# [Linux] Bash standaard ls: lijst bestanden en mappen

## Overzicht
De `ls`-opdracht in Bash wordt gebruikt om de inhoud van een directory weer te geven. Het toont een lijst van bestanden en mappen, waardoor gebruikers snel kunnen zien wat er in een specifieke map aanwezig is.

## Gebruik
De basis syntaxis van de `ls`-opdracht is als volgt:

```bash
ls [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Toont de inhoud in een lange lijstweergave, inclusief details zoals permissies, eigenaar, grootte en datum.
- `-a`: Toont ook verborgen bestanden (bestanden die beginnen met een punt).
- `-h`: Toont bestandsgroottes in een leesbaar formaat (bijv. K, M, G).
- `-R`: Toont de inhoud van subdirectories recursief.
- `-t`: Sorteert bestanden op tijd, met de meest recente eerst.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ls`-opdracht:

1. Gewone lijst van bestanden en mappen:
   ```bash
   ls
   ```

2. Lijst met verborgen bestanden:
   ```bash
   ls -a
   ```

3. Lange lijstweergave met details:
   ```bash
   ls -l
   ```

4. Lijst met leesbare bestandsgroottes:
   ```bash
   ls -lh
   ```

5. Recursieve lijst van bestanden en mappen:
   ```bash
   ls -R
   ```

6. Lijst van bestanden gesorteerd op tijd:
   ```bash
   ls -lt
   ```

## Tips
- Gebruik `ls -la` om een uitgebreide lijst van alle bestanden, inclusief verborgen bestanden, te krijgen.
- Combineer opties voor meer gedetailleerde output, bijvoorbeeld `ls -lhR` voor een lange lijstweergave met leesbare groottes, inclusief subdirectories.
- Gebruik de tab-toets voor autocompletion om snel door bestanden en mappen te navigeren.