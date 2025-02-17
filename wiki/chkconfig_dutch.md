# [Linux] Bash chkconfig gebruik: Beheer van systeemdiensten

## Overzicht
Het `chkconfig` commando wordt gebruikt om de opstartinstellingen van systeemdiensten in Linux te beheren. Het stelt gebruikers in staat om te configureren welke diensten automatisch moeten starten bij het opstarten van het systeem en in welke runlevels deze diensten actief moeten zijn.

## Gebruik
De basis syntaxis van het `chkconfig` commando is als volgt:

```bash
chkconfig [opties] [argumenten]
```

## Veelvoorkomende Opties
- `--list`: Toont de huidige status van alle diensten.
- `--add`: Voegt een nieuwe dienst toe aan de opstartconfiguratie.
- `--remove`: Verwijdert een dienst uit de opstartconfiguratie.
- `--level`: Specificeert de runlevels voor de opgegeven dienst.
- `on`: Zet de dienst aan voor de opgegeven runlevels.
- `off`: Zet de dienst uit voor de opgegeven runlevels.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `chkconfig`:

1. **Lijst alle diensten en hun status:**
   ```bash
   chkconfig --list
   ```

2. **Voeg een nieuwe dienst toe:**
   ```bash
   chkconfig --add myservice
   ```

3. **Verwijder een dienst:**
   ```bash
   chkconfig --remove myservice
   ```

4. **Zet een dienst aan voor specifieke runlevels (bijv. 2, 3, 4):**
   ```bash
   chkconfig myservice on --level 234
   ```

5. **Zet een dienst uit voor specifieke runlevels (bijv. 5):**
   ```bash
   chkconfig myservice off --level 5
   ```

## Tips
- Controleer altijd de status van een dienst met `chkconfig --list` voordat je wijzigingen aanbrengt.
- Gebruik `chkconfig` met voorzichtigheid, vooral bij het verwijderen van diensten, om te voorkomen dat je belangrijke systeemfunctionaliteit uitschakelt.
- Vergeet niet om na het toevoegen of verwijderen van diensten het systeem opnieuw op te starten om de wijzigingen van kracht te laten worden.