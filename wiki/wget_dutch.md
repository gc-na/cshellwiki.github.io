# [Linux] C Shell (csh) wget gebruik: Bestanden downloaden van het web

## Overzicht
De `wget`-opdracht is een krachtige tool die wordt gebruikt om bestanden van het internet te downloaden. Het ondersteunt verschillende protocollen zoals HTTP, HTTPS en FTP, en kan worden gebruikt voor zowel eenvoudige downloads als complexe taken zoals het mirroren van websites.

## Gebruik
De basis syntaxis van de `wget`-opdracht is als volgt:

```
wget [opties] [argumenten]
```

## Veelvoorkomende opties
- `-O <bestand>`: Sla het gedownloade bestand op met de opgegeven naam.
- `-q`: Voer de opdracht uit in stille modus, zonder uitvoer naar het scherm.
- `-r`: Download bestanden recursief, wat handig is voor het mirroren van websites.
- `-c`: Hervat een onderbroken download.
- `--limit-rate=<snelheid>`: Beperk de downloadsnelheid tot de opgegeven waarde.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `wget`:

1. **Een enkel bestand downloaden:**
   ```bash
   wget https://example.com/bestand.zip
   ```

2. **Een bestand opslaan met een andere naam:**
   ```bash
   wget -O nieuwe_naam.zip https://example.com/bestand.zip
   ```

3. **Downloaden in stille modus:**
   ```bash
   wget -q https://example.com/bestand.zip
   ```

4. **Recursief downloaden van een website:**
   ```bash
   wget -r https://example.com/
   ```

5. **Een onderbroken download hervatten:**
   ```bash
   wget -c https://example.com/bestand.zip
   ```

6. **De downloadsnelheid beperken:**
   ```bash
   wget --limit-rate=200k https://example.com/bestand.zip
   ```

## Tips
- Gebruik de `-q` optie voor stille downloads als je niet wilt dat de terminal volloopt met uitvoer.
- Combineer de `-r` optie met `-np` (no parent) om te voorkomen dat je naar bovenliggende mappen in de directorystructuur gaat.
- Controleer altijd de downloadlink voordat je een bestand downloadt om te zorgen dat het veilig is.