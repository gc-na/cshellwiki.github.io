# [Linux] C Shell (csh) df Gebruik: Toont schijfruimte-informatie

## Overzicht
De `df` (disk free) opdracht in C Shell toont informatie over de beschikbare en gebruikte schijfruimte op bestandssystemen. Het is een nuttige tool voor systeembeheerders en gebruikers die willen controleren hoeveel ruimte er nog beschikbaar is op hun schijven.

## Gebruik
De basis syntaxis van de `df` opdracht is als volgt:

```csh
df [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont de schijfruimte in een leesbaar formaat (bijvoorbeeld in KB, MB of GB).
- `-T`: Toont het type van het bestandssysteem.
- `-a`: Toont informatie over alle bestandssystemen, inclusief die met een gebruik van 0.
- `-i`: Toont informatie over inodes in plaats van schijfruimte.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `df` opdracht:

1. Toon de schijfruimte in een leesbaar formaat:

    ```csh
    df -h
    ```

2. Toon het type van het bestandssysteem:

    ```csh
    df -T
    ```

3. Toon informatie over alle bestandssystemen:

    ```csh
    df -a
    ```

4. Toon informatie over inodes:

    ```csh
    df -i
    ```

## Tips
- Gebruik de `-h` optie voor een gemakkelijk te begrijpen weergave van schijfruimte, vooral als je met grote schijven werkt.
- Controleer regelmatig de schijfruimte om te voorkomen dat je schijven vol raken, wat kan leiden tot systeemproblemen.
- Combineer `df` met andere opdrachten zoals `grep` om specifieke informatie te filteren, bijvoorbeeld:

    ```csh
    df -h | grep /dev/sda1
    ```