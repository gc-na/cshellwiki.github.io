# [Linux] Bash tar gebruik: Bestanden archiveren en comprimeren

## Overzicht
De `tar`-opdracht, wat staat voor "tape archive", is een veelgebruikte tool in Linux en andere Unix-achtige systemen voor het archiveren van bestanden. Het stelt gebruikers in staat om meerdere bestanden en mappen samen te voegen in één enkel archiefbestand, wat het beheer en de distributie vergemakkelijkt. Daarnaast kan `tar` ook worden gebruikt om bestanden te comprimeren.

## Gebruik
De basis syntaxis van de `tar`-opdracht is als volgt:

```bash
tar [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelgebruikte opties voor de `tar`-opdracht:

- `-c`: Maak een nieuw archief.
- `-x`: Extraheer bestanden uit een archief.
- `-f`: Specificeer de naam van het archiefbestand.
- `-v`: Toon de voortgang (verbose mode).
- `-z`: Comprimeer of decomprimeer met gzip.
- `-j`: Comprimeer of decomprimeer met bzip2.

## Veelvoorkomende Voorbeelden

### Een archief maken
Om een archief te maken van een map genaamd `mijnmap` en het op te slaan als `mijnarchief.tar`, gebruik je:

```bash
tar -cvf mijnarchief.tar mijnmap
```

### Een archief extraheren
Om een archief genaamd `mijnarchief.tar` te extraheren, gebruik je:

```bash
tar -xvf mijnarchief.tar
```

### Een gecomprimeerd archief maken met gzip
Om een gecomprimeerd archief te maken met gzip, gebruik je:

```bash
tar -czvf mijnarchief.tar.gz mijnmap
```

### Een gecomprimeerd archief extraheren met gzip
Om een gecomprimeerd archief te extraheren, gebruik je:

```bash
tar -xzvf mijnarchief.tar.gz
```

## Tips
- Gebruik de `-v` optie voor een duidelijke weergave van welke bestanden worden toegevoegd of geëxtraheerd.
- Controleer altijd de inhoud van een archief met de `-t` optie voordat je het extraheert:

  ```bash
  tar -tvf mijnarchief.tar
  ```

- Overweeg om `gzip` of `bzip2` te gebruiken voor compressie om schijfruimte te besparen, vooral voor grote archieven.