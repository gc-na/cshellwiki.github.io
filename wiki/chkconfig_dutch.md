# [Linux] C Shell (csh) chkconfig gebruik: Beheer van systeemdiensten

## Overzicht
De `chkconfig` opdracht wordt gebruikt om de opstartinstellingen van systeemdiensten in Linux te beheren. Hiermee kun je diensten in- of uitschakelen bij het opstarten van het systeem.

## Gebruik
De basis syntaxis van de `chkconfig` opdracht is als volgt:

```bash
chkconfig [opties] [argumenten]
```

## Veelvoorkomende Opties
- `--list`: Toon de huidige status van alle diensten.
- `--add`: Voeg een nieuwe dienst toe aan de opstartinstellingen.
- `--del`: Verwijder een dienst uit de opstartinstellingen.
- `--level`: Specificeer de runlevels voor de dienst.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `chkconfig`:

1. **Lijst alle diensten en hun status:**
   ```bash
   chkconfig --list
   ```

2. **Voeg een nieuwe dienst toe:**
   ```bash
   chkconfig --add naam_van_dienst
   ```

3. **Verwijder een dienst uit de opstartinstellingen:**
   ```bash
   chkconfig --del naam_van_dienst
   ```

4. **Schakel een dienst in voor specifieke runlevels:**
   ```bash
   chkconfig naam_van_dienst on --level 2345
   ```

5. **Schakel een dienst uit voor specifieke runlevels:**
   ```bash
   chkconfig naam_van_dienst off --level 2345
   ```

## Tips
- Controleer altijd de status van een dienst na het aanbrengen van wijzigingen met `chkconfig --list`.
- Gebruik de `--level` optie om specifiek te zijn over welke runlevels je wilt aanpassen, zodat je geen onbedoelde wijzigingen aanbrengt.
- Wees voorzichtig bij het verwijderen van diensten; zorg ervoor dat je weet wat de dienst doet voordat je deze verwijdert.