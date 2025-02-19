# [Linux] C Shell (csh) who gebruik: Toon ingelogde gebruikers

## Overzicht
De `who` opdracht in C Shell toont een lijst van gebruikers die momenteel zijn ingelogd op het systeem. Het geeft informatie zoals de gebruikersnaam, terminal, inlogtijd en soms het IP-adres of de hostnaam.

## Gebruik
De basis syntaxis van de `who` opdracht is als volgt:

```
who [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Toont de tijd van de laatste systeemopstart.
- `-q`: Toont alleen de gebruikersnamen en het aantal ingelogde gebruikers.
- `-H`: Toont de kopteksten voor de uitvoer.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik**: Toont alle ingelogde gebruikers.
   ```csh
   who
   ```

2. **Toon de laatste opstarttijd van het systeem**:
   ```csh
   who -b
   ```

3. **Toon alleen het aantal ingelogde gebruikers**:
   ```csh
   who -q
   ```

4. **Toon de uitvoer met kopteksten**:
   ```csh
   who -H
   ```

## Tips
- Gebruik `who` in combinatie met andere opdrachten zoals `grep` om specifieke gebruikers te filteren.
- Controleer regelmatig de ingelogde gebruikers om ongeautoriseerde toegang te detecteren.
- Combineer `who` met `wc -l` om snel het aantal ingelogde gebruikers te tellen:
  ```csh
  who | wc -l
  ```