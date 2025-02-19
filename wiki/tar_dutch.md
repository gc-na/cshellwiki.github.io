# [Linux] C Shell (csh) tar Gebruik: Archiveren en comprimeren van bestanden

## Overzicht
De `tar`-opdracht, wat staat voor "tape archive", wordt gebruikt om meerdere bestanden en mappen samen te voegen in één enkel archiefbestand. Dit is handig voor back-ups en het delen van bestanden.

## Gebruik
De basis syntaxis van de `tar`-opdracht is als volgt:

```csh
tar [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Maak een nieuw archief.
- `-x`: Extraheer bestanden uit een archief.
- `-f`: Geef de naam van het archiefbestand op.
- `-v`: Toon gedetailleerde uitvoer (verbose).
- `-z`: Comprimeer of decomprimeer met gzip.

## Veelvoorkomende Voorbeelden

### 1. Een nieuw archief maken
Om een archief genaamd `mijnbestanden.tar` te maken van de map `mijnmap`:

```csh
tar -cvf mijnbestanden.tar mijnmap
```

### 2. Een archief extraheren
Om de inhoud van `mijnbestanden.tar` te extraheren:

```csh
tar -xvf mijnbestanden.tar
```

### 3. Een gecomprimeerd archief maken
Om een gecomprimeerd archief met gzip te maken:

```csh
tar -czvf mijnbestanden.tar.gz mijnmap
```

### 4. Een gecomprimeerd archief extraheren
Om een gecomprimeerd archief te extraheren:

```csh
tar -xzvf mijnbestanden.tar.gz
```

## Tips
- Gebruik de `-v` optie voor gedetailleerde uitvoer, zodat je kunt zien welke bestanden worden verwerkt.
- Controleer altijd de inhoud van een archief met `tar -tvf archief.tar` voordat je bestanden extraheert.
- Overweeg om gecomprimeerde archieven te gebruiken om schijfruimte te besparen, vooral bij grote datasets.