# [Linux] C Shell (csh) update-rc.d gebruik: Beheer van opstartscripts

## Overzicht
Het `update-rc.d` commando wordt gebruikt om opstartscripts te beheren in Debian-gebaseerde systemen. Het stelt gebruikers in staat om scripts toe te voegen, te verwijderen of te configureren voor het opstarten en afsluiten van services.

## Gebruik
De basis syntaxis van het commando is als volgt:

```csh
update-rc.d [opties] [argumenten]
```

## Veelvoorkomende Opties
- `defaults`: Voegt het script toe met standaardinstellingen voor opstart- en afsluitvolgorde.
- `remove`: Verwijdert het script uit de opstartconfiguratie.
- `enable`: Schakelt het script in voor opstarten.
- `disable`: Schakelt het script uit voor opstarten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `update-rc.d`:

1. **Voeg een script toe met standaardinstellingen**:
    ```csh
    update-rc.d mijn-service defaults
    ```

2. **Verwijder een script uit de opstartconfiguratie**:
    ```csh
    update-rc.d mijn-service remove
    ```

3. **Schakel een script in voor opstarten**:
    ```csh
    update-rc.d mijn-service enable
    ```

4. **Schakel een script uit voor opstarten**:
    ```csh
    update-rc.d mijn-service disable
    ```

## Tips
- Zorg ervoor dat je de juiste rechten hebt om `update-rc.d` uit te voeren; meestal zijn root-rechten vereist.
- Controleer altijd de status van je scripts na het toevoegen of verwijderen om te bevestigen dat ze correct zijn ingesteld.
- Gebruik `man update-rc.d` om meer gedetailleerde informatie en opties te bekijken.