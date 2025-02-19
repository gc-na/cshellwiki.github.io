# [Linux] C Shell (csh) cd gebruik: Verander van directory

## Overzicht
De `cd` (change directory) opdracht in C Shell wordt gebruikt om de huidige werkdirectory te wijzigen. Dit stelt gebruikers in staat om naar verschillende mappen binnen het bestandssysteem te navigeren.

## Gebruik
De basisstructuur van de `cd` opdracht is als volgt:

```csh
cd [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-` : Ga terug naar de vorige directory.
- `~` : Ga naar de home directory van de gebruiker.
- `..` : Ga naar de bovenliggende directory van de huidige directory.

## Veelvoorkomende Voorbeelden
- Ga naar de home directory:
  ```csh
  cd ~
  ```

- Ga naar een specifieke directory, bijvoorbeeld `documenten`:
  ```csh
  cd documenten
  ```

- Ga naar de bovenliggende directory:
  ```csh
  cd ..
  ```

- Ga terug naar de vorige directory:
  ```csh
  cd -
  ```

## Tips
- Gebruik `cd` zonder argumenten om snel naar je home directory te gaan.
- Controleer altijd je huidige directory met de `pwd` (print working directory) opdracht na het gebruik van `cd`.
- Gebruik tab-completion om snel naar directories te navigeren zonder de volledige naam in te voeren.