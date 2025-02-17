# [Linux] Bash groupmod gebruik: Groep wijzigen

## Overzicht
De `groupmod` opdracht wordt gebruikt om bestaande groepen in een Linux-systeem te wijzigen. Hiermee kunnen beheerders de eigenschappen van een groep aanpassen, zoals de groepsnaam of het groeps-ID.

## Gebruik
De basis syntaxis van de `groupmod` opdracht is als volgt:

```bash
groupmod [opties] [argumenten]
```

## Veelvoorkomende opties
- `-n, --new-name NEW_GROUP`: Wijzig de naam van de groep naar NEW_GROUP.
- `-g, --gid GID`: Wijzig het groeps-ID naar GID.
- `-o, --non-unique`: Sta toe dat het nieuwe groeps-ID niet uniek is (gebruik dit met voorzichtigheid).

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Groepsnaam wijzigen
Om de naam van een groep van `oudenaam` naar `nieuwenaam` te wijzigen, gebruik je de volgende opdracht:

```bash
groupmod -n nieuwenaam oudenaam
```

### Voorbeeld 2: Groeps-ID wijzigen
Om het groeps-ID van een groep te wijzigen naar 1001, gebruik je deze opdracht:

```bash
groupmod -g 1001 groepsnaam
```

### Voorbeeld 3: Groepsnaam en ID tegelijk wijzigen
Je kunt ook zowel de naam als het ID van een groep in één opdracht wijzigen:

```bash
groupmod -n nieuwenaam -g 1002 oudenaam
```

## Tips
- Zorg ervoor dat je de juiste rechten hebt om de `groupmod` opdracht uit te voeren; meestal zijn root-rechten vereist.
- Controleer altijd of de nieuwe groepsnaam of ID al in gebruik is om conflicten te voorkomen.
- Gebruik de `getent group` opdracht om de huidige groepen en hun instellingen te bekijken voordat je wijzigingen aanbrengt.