# [Linux] Bash who gebruik: Toon ingelogde gebruikers

## Overzicht
De `who` opdracht in Bash toont een lijst van gebruikers die momenteel zijn ingelogd op het systeem. Het geeft informatie zoals de gebruikersnaam, terminal, inlogtijd en soms het IP-adres of de hostnaam van de gebruiker.

## Gebruik
De basis syntaxis van de `who` opdracht is als volgt:

```bash
who [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Toont alle beschikbare informatie, inclusief inlog- en afwezigheidsinformatie.
- `-b`: Toont de tijd van de laatste systeemopstart.
- `-q`: Toont alleen de gebruikersnamen en het aantal ingelogde gebruikers.
- `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `who` opdracht:

1. **Basisgebruik**: Toont de lijst van ingelogde gebruikers.
   ```bash
   who
   ```

2. **Toon alle informatie**: Gebruik de `-a` optie voor gedetailleerde informatie.
   ```bash
   who -a
   ```

3. **Laatste opstarttijd**: Gebruik de `-b` optie om de laatste opstarttijd van het systeem te zien.
   ```bash
   who -b
   ```

4. **Aantal ingelogde gebruikers**: Gebruik de `-q` optie om alleen de gebruikersnamen en het aantal in te loggen gebruikers te tonen.
   ```bash
   who -q
   ```

## Tips
- Gebruik `who` in combinatie met andere opdrachten zoals `grep` om specifieke gebruikers te filteren.
- Combineer `who` met `wc -l` om het totale aantal ingelogde gebruikers te tellen:
  ```bash
  who | wc -l
  ```
- Houd rekening met de tijdzone-instellingen van je systeem, aangezien de inlogtijden kunnen variëren afhankelijk van de configuratie.