# [Linux] Bash chmod gebruik: Wijzig bestandspermissies

## Overzicht
De `chmod` (change mode) opdracht in Bash wordt gebruikt om de bestandspermissies van bestanden en mappen te wijzigen. Hiermee kun je bepalen wie toegang heeft tot een bestand en welke acties zij kunnen uitvoeren, zoals lezen, schrijven of uitvoeren.

## Gebruik
De basis syntaxis van de `chmod` opdracht is als volgt:

```bash
chmod [opties] [argumenten]
```

## Veelvoorkomende opties
- `-R`: Wijzig de permissies recursief voor alle bestanden en submappen in de opgegeven map.
- `u`: Verwijst naar de eigenaar van het bestand (user).
- `g`: Verwijst naar de groep van het bestand (group).
- `o`: Verwijst naar anderen (others).
- `+`: Voegt een permissie toe.
- `-`: Verwijdert een permissie.
- `=`: Stelt een specifieke permissie in.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `chmod`:

1. **Geef de eigenaar lees- en schrijfrechten:**
   ```bash
   chmod u+rw bestandsnaam.txt
   ```

2. **Verwijder uitvoerrechten voor anderen:**
   ```bash
   chmod o-x script.sh
   ```

3. **Geef iedereen leesrechten:**
   ```bash
   chmod a+r document.pdf
   ```

4. **Wijzig de permissies recursief voor een map:**
   ```bash
   chmod -R 755 /pad/naar/map
   ```

5. **Stel specifieke permissies in voor een bestand:**
   ```bash
   chmod 644 bestand.txt
   ```

## Tips
- Gebruik `ls -l` om de huidige permissies van bestanden en mappen te bekijken voordat je wijzigingen aanbrengt.
- Wees voorzichtig met het geven van uitvoerrechten aan bestanden, vooral bij scripts, om onbedoelde uitvoer te voorkomen.
- Maak gebruik van de recursieve optie `-R` met beleid, omdat dit ook de permissies van alle onderliggende bestanden en mappen wijzigt.