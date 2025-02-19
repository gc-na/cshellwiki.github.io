# [Linux] C Shell (csh) rpm gebruik: Beheer van RPM-pakketten

## Overzicht
De `rpm`-opdracht wordt gebruikt voor het beheren van RPM-pakketten op Linux-systemen. Het stelt gebruikers in staat om software te installeren, te verwijderen, te upgraden en informatie over geïnstalleerde pakketten op te vragen.

## Gebruik
De basis syntaxis van de `rpm`-opdracht is als volgt:

```
rpm [opties] [argumenten]
```

## Veelvoorkomende opties
- `-i`: Installeer een nieuw pakket.
- `-e`: Verwijder een geïnstalleerd pakket.
- `-U`: Upgrade een bestaand pakket naar een nieuwere versie.
- `-q`: Vraag informatie op over geïnstalleerde pakketten.
- `-v`: Toon gedetailleerde uitvoer (verbose).
- `-h`: Toon voortgang in de vorm van een voortgangsbalk (hash).

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `rpm`-opdracht:

### Een pakket installeren
```bash
rpm -i pakketnaam.rpm
```

### Een pakket verwijderen
```bash
rpm -e pakketnaam
```

### Een pakket upgraden
```bash
rpm -U pakketnaam.rpm
```

### Informatie opvragen over een geïnstalleerd pakket
```bash
rpm -q pakketnaam
```

### Gedetailleerde informatie over een pakket
```bash
rpm -qi pakketnaam
```

## Tips
- Zorg ervoor dat je de juiste rechten hebt (bijvoorbeeld als root) bij het installeren of verwijderen van pakketten.
- Gebruik de `-v` en `-h` opties samen voor meer inzicht in het installatieproces.
- Controleer altijd de afhankelijkheden van een pakket voordat je het installeert of verwijdert om problemen te voorkomen.