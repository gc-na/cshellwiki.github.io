# [Linux] Bash logout gebruik: Sluit de huidige shell-sessie af

## Overzicht
De `logout` opdracht wordt gebruikt om de huidige shell-sessie af te sluiten. Dit is vooral nuttig wanneer je werkt in een interactieve shell, zoals een terminalvenster of een SSH-sessie. Het beëindigen van de sessie zorgt ervoor dat alle processen die aan die sessie zijn gekoppeld, worden afgesloten.

## Gebruik
De basis syntaxis van de `logout` opdracht is als volgt:

```bash
logout [options]
```

## Veelvoorkomende Opties
De `logout` opdracht heeft geen specifieke opties, maar het is belangrijk om te weten dat het alleen werkt in een login shell. Als je het probeert uit te voeren in een niet-login shell, krijg je een foutmelding.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudig afmelden
Om je huidige shell-sessie af te sluiten, typ je eenvoudig:

```bash
logout
```

### Voorbeeld 2: Afmelden vanuit een SSH-sessie
Als je bent ingelogd op een externe server via SSH en je wilt de sessie beëindigen, gebruik je:

```bash
logout
```

### Voorbeeld 3: Afmelden in een subshell
Als je een subshell hebt geopend (bijvoorbeeld met `bash`), kun je deze afsluiten met:

```bash
logout
```

## Tips
- Zorg ervoor dat je al je werk hebt opgeslagen voordat je `logout` gebruikt, omdat alle niet-opgeslagen gegevens verloren gaan.
- Gebruik `exit` als je een subshell wilt afsluiten zonder een foutmelding te krijgen in een niet-login shell.
- Controleer of je geen actieve processen hebt die je wilt behouden voordat je de sessie beëindigt.