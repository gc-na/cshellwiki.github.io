# [Linux] Bash rmdir gebruik: Verwijder lege mappen

## Overzicht
De `rmdir` opdracht in Bash wordt gebruikt om lege directories te verwijderen. Het is een eenvoudige maar krachtige tool voor het beheren van je bestandssysteem.

## Gebruik
De basis syntaxis van de `rmdir` opdracht is als volgt:

```bash
rmdir [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-p`: Verwijdert de opgegeven directory en, indien leeg, ook de bovenliggende directories.
- `--ignore-fail-on-non-empty`: Negeert fouten als de directory niet leeg is.

## Veelvoorkomende Voorbeelden

### Een lege directory verwijderen
Om een lege directory genaamd `mijnmap` te verwijderen, gebruik je:

```bash
rmdir mijnmap
```

### Meerdere lege directories verwijderen
Je kunt ook meerdere lege directories in één opdracht verwijderen:

```bash
rmdir map1 map2 map3
```

### Een lege directory en zijn bovenliggende lege directories verwijderen
Als je een directory genaamd `submap` hebt binnen `hoofdmmap` en beide zijn leeg, kun je ze als volgt verwijderen:

```bash
rmdir -p hoofdmmap/submap
```

## Tips
- Zorg ervoor dat de directory leeg is voordat je `rmdir` gebruikt, anders krijg je een foutmelding.
- Gebruik de `-p` optie om ook bovenliggende lege directories in één keer te verwijderen.
- Controleer altijd de inhoud van een directory met `ls` voordat je deze verwijdert om onbedoeld verlies van gegevens te voorkomen.