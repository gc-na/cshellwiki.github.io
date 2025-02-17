# [Linux] Bash rpm gebruik: Beheer van RPM-pakketten

## Overzicht
Het `rpm`-commando (Red Hat Package Manager) wordt gebruikt voor het beheren van RPM-pakketten op Linux-systemen. Het stelt gebruikers in staat om software te installeren, te verwijderen, te upgraden en informatie over geïnstalleerde pakketten op te vragen.

## Gebruik
De basis syntaxis van het `rpm`-commando is als volgt:

```bash
rpm [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i` : Installeer een nieuw RPM-pakket.
- `-e` : Verwijder een geïnstalleerd RPM-pakket.
- `-U` : Upgrade een geïnstalleerd pakket naar een nieuwere versie.
- `-q` : Vraag informatie op over een geïnstalleerd pakket.
- `-l` : Toon de bestanden die bij een geïnstalleerd pakket horen.

## Veelvoorkomende Voorbeelden

### Een pakket installeren
Om een RPM-pakket te installeren, gebruik je de volgende opdracht:

```bash
rpm -i pakketnaam.rpm
```

### Een pakket verwijderen
Om een geïnstalleerd pakket te verwijderen, gebruik je:

```bash
rpm -e pakketnaam
```

### Een pakket upgraden
Om een pakket te upgraden naar een nieuwere versie, gebruik je:

```bash
rpm -U pakketnaam.rpm
```

### Informatie opvragen over een geïnstalleerd pakket
Om informatie over een geïnstalleerd pakket op te vragen, gebruik je:

```bash
rpm -q pakketnaam
```

### Lijst van bestanden in een pakket
Om de bestanden te tonen die bij een geïnstalleerd pakket horen, gebruik je:

```bash
rpm -ql pakketnaam
```

## Tips
- Zorg ervoor dat je de juiste rechten hebt (gebruik `sudo` indien nodig) bij het installeren of verwijderen van pakketten.
- Controleer altijd de afhankelijkheden van een pakket voordat je het installeert of verwijdert.
- Gebruik de `-v` (verbose) optie voor meer gedetailleerde uitvoer tijdens het uitvoeren van commando's.