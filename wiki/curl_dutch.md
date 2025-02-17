# [Linux] Bash curl gebruik: Haal gegevens op van een server

## Overzicht
De `curl`-opdracht is een krachtige tool die wordt gebruikt om gegevens van of naar een server te verzenden. Het ondersteunt verschillende protocollen, waaronder HTTP, HTTPS, FTP en meer. Met `curl` kun je eenvoudig bestanden downloaden, API-aanroepen doen en gegevens verzenden.

## Gebruik
De basis syntaxis van de `curl`-opdracht is als volgt:

```bash
curl [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelgebruikte opties voor `curl`:

- `-O`: Download een bestand en geef het dezelfde naam als op de server.
- `-o <bestandsnaam>`: Download een bestand en sla het op met de opgegeven naam.
- `-I`: Haal alleen de HTTP-header op.
- `-X <methode>`: Specificeer de HTTP-methode (bijvoorbeeld GET, POST).
- `-d <gegevens>`: Stuur gegevens als een POST-verzoek.
- `-H <header>`: Voeg een aangepaste header toe aan de aanvraag.

## Veelvoorkomende Voorbeelden

### 1. Een bestand downloaden
Om een bestand van een URL te downloaden en het op te slaan met dezelfde naam:

```bash
curl -O http://example.com/bestand.txt
```

### 2. Een bestand opslaan met een specifieke naam
Om een bestand te downloaden en het op te slaan met een andere naam:

```bash
curl -o mijn_bestand.txt http://example.com/bestand.txt
```

### 3. Alleen de HTTP-header ophalen
Om alleen de HTTP-header van een URL op te halen:

```bash
curl -I http://example.com
```

### 4. Gegevens verzenden met een POST-verzoek
Om gegevens te verzenden met een POST-verzoek:

```bash
curl -X POST -d "naam=John&leeftijd=30" http://example.com/api
```

### 5. Een aangepaste header toevoegen
Om een aangepaste header toe te voegen aan je verzoek:

```bash
curl -H "Authorization: Bearer jouw_token" http://example.com/secure-endpoint
```

## Tips
- Gebruik de `-v` optie voor gedetailleerde uitvoer van het verzoek en de respons, wat handig kan zijn voor foutopsporing.
- Combineer opties om complexe verzoeken te maken, zoals het verzenden van gegevens met aangepaste headers.
- Controleer altijd de documentatie van de API die je gebruikt voor specifieke vereisten met betrekking tot headers en gegevensformaten.