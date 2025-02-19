# [Linux] C Shell (csh) yum gebruik: Beheer van softwarepakketten

## Overzicht
De `yum`-opdracht is een pakketbeheerder voor Linux-distributies die RPM-pakketten gebruikt. Het stelt gebruikers in staat om softwarepakketten te installeren, bij te werken en te verwijderen, evenals om afhankelijkheden te beheren.

## Gebruik
De basis syntaxis van de `yum`-opdracht is als volgt:

```bash
yum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `install`: Installeert een nieuw pakket.
- `remove`: Verwijdert een geïnstalleerd pakket.
- `update`: Update een geïnstalleerd pakket naar de nieuwste versie.
- `search`: Zoekt naar pakketten in de repository.
- `list`: Lijst beschikbare of geïnstalleerde pakketten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `yum`:

1. **Een pakket installeren**:
   ```bash
   yum install pakketnaam
   ```

2. **Een pakket verwijderen**:
   ```bash
   yum remove pakketnaam
   ```

3. **Een pakket bijwerken**:
   ```bash
   yum update pakketnaam
   ```

4. **Zoeken naar een pakket**:
   ```bash
   yum search zoekterm
   ```

5. **Lijst van geïnstalleerde pakketten**:
   ```bash
   yum list installed
   ```

## Tips
- Zorg ervoor dat je altijd de laatste versie van de repository's hebt door `yum update` regelmatig uit te voeren.
- Gebruik `yum clean all` om ongebruikte gegevens te verwijderen en schijfruimte vrij te maken.
- Controleer altijd de afhankelijkheden van een pakket voordat je het installeert of verwijdert om problemen te voorkomen.