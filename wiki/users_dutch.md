# [Linux] Bash gebruikersgebruik: Toon gebruikersinformatie

## Overzicht
De `users` opdracht in Bash toont een lijst van gebruikers die momenteel zijn ingelogd op het systeem. Het geeft een eenvoudige manier om te zien wie er actief is zonder gedetailleerde informatie over elke gebruiker te tonen.

## Gebruik
De basis syntaxis van de `users` opdracht is als volgt:

```bash
users [opties]
```

## Veelvoorkomende opties
De `users` opdracht heeft geen specifieke opties, maar het kan in combinatie met andere opdrachten worden gebruikt voor meer geavanceerde functionaliteit.

## Veelvoorkomende Voorbeelden

1. **Toon ingelogde gebruikers:**
   Dit is de meest basale manier om de ingelogde gebruikers te bekijken.
   ```bash
   users
   ```

2. **Gebruik met andere opdrachten:**
   Je kunt de uitvoer van `users` doorsturen naar andere opdrachten, zoals `sort` om een gesorteerde lijst van gebruikers te krijgen.
   ```bash
   users | sort
   ```

3. **Opslaan van gebruikers in een bestand:**
   Je kunt de lijst van ingelogde gebruikers opslaan in een tekstbestand voor later gebruik.
   ```bash
   users > ingelogde_gebruikers.txt
   ```

## Tips
- Gebruik `who` of `w` als je meer gedetailleerde informatie over ingelogde gebruikers wilt, zoals hun inlogtijd en actieve sessies.
- Combineer `users` met andere commando's in een script om automatisch rapporten te genereren over actieve gebruikers.
- Houd er rekening mee dat de uitvoer van `users` een lijst met gebruikersnamen geeft, gescheiden door spaties, wat handig kan zijn voor verdere verwerking.