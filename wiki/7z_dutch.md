# [Nederlandse] C Shell (csh) 7z Gebruik: Bestandcompressie en -decompressie

## Overzicht
De 7z-opdracht is een krachtige tool voor het comprimeren en decomprimeren van bestanden en mappen. Het ondersteunt verschillende archiefformaten en biedt hoge compressieverhoudingen, waardoor het een populaire keuze is voor het beheren van bestanden.

## Gebruik
De basis syntaxis van de 7z-opdracht is als volgt:

```
7z [opties] [argumenten]
```

## Veelvoorkomende Opties
- `a`: Voeg bestanden toe aan een archief.
- `x`: Extraheer bestanden uit een archief.
- `l`: Lijst de inhoud van een archief.
- `d`: Verwijder bestanden uit een archief.
- `t`: Test de integriteit van een archief.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de 7z-opdracht:

### Archiveren van bestanden
Om bestanden te comprimeren in een archief genaamd `mijnarchief.7z`, gebruik je:

```
7z a mijnarchief.7z bestand1.txt bestand2.txt
```

### Decompressie van een archief
Om bestanden uit `mijnarchief.7z` te extraheren, gebruik je:

```
7z x mijnarchief.7z
```

### Lijst van bestanden in een archief
Om de inhoud van `mijnarchief.7z` te bekijken, gebruik je:

```
7z l mijnarchief.7z
```

### Verwijderen van bestanden uit een archief
Om `bestand1.txt` uit `mijnarchief.7z` te verwijderen, gebruik je:

```
7z d mijnarchief.7z bestand1.txt
```

### Testen van een archief
Om de integriteit van `mijnarchief.7z` te testen, gebruik je:

```
7z t mijnarchief.7z
```

## Tips
- Zorg ervoor dat je de juiste opties gebruikt om ongewenste gegevensverlies te voorkomen.
- Gebruik de `-p` optie om een wachtwoord toe te voegen aan je archief voor extra beveiliging.
- Maak regelmatig back-ups van belangrijke archieven om gegevensverlies te voorkomen.