# [Linux] Bash wget gebruik: Bestanden downloaden van het web

## Overzicht
De `wget`-opdracht is een krachtige tool in de Bash-omgeving die wordt gebruikt om bestanden van het internet te downloaden. Het ondersteunt verschillende protocollen, waaronder HTTP, HTTPS en FTP, en kan worden gebruikt voor zowel eenvoudige downloads als meer geavanceerde taken zoals het downloaden van volledige websites.

## Gebruik
De basis syntaxis van de `wget`-opdracht is als volgt:
```bash
wget [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-O <bestand>`: Sla het gedownloade bestand op met een specifieke naam.
- `-c`: Hervat een onderbroken download.
- `-r`: Download bestanden recursief (bijvoorbeeld voor het downloaden van een hele website).
- `-p`: Download alle benodigde bestanden om een webpagina correct weer te geven (zoals afbeeldingen en CSS).
- `--limit-rate=<snelheid>`: Beperk de downloadsnelheid tot een bepaalde waarde.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `wget`:

1. **Een enkel bestand downloaden:**
   ```bash
   wget https://example.com/bestand.zip
   ```

2. **Een bestand opslaan met een specifieke naam:**
   ```bash
   wget -O mijn_bestand.zip https://example.com/bestand.zip
   ```

3. **Een download hervatten:**
   ```bash
   wget -c https://example.com/groot_bestand.zip
   ```

4. **Een hele website downloaden:**
   ```bash
   wget -r https://example.com
   ```

5. **Alle benodigde bestanden voor een webpagina downloaden:**
   ```bash
   wget -p https://example.com/pagina.html
   ```

## Tips
- Gebruik de optie `-q` voor stille downloads, zodat er geen output naar de terminal wordt gestuurd.
- Combineer de `-r` en `--limit-rate` opties om grote websites efficiënt te downloaden zonder je bandbreedte te overbelasten.
- Controleer altijd de rechten en het beleid van de website voordat je grote hoeveelheden gegevens downloadt, om te voorkomen dat je de server overbelast.