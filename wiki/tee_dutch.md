# [Linux] Bash tee gebruik: Schrijf naar standaarduitvoer en bestanden

## Overzicht
De `tee`-opdracht in Bash wordt gebruikt om de standaarduitvoer van een commando te splitsen. Het schrijft de uitvoer naar zowel de standaarduitvoer (meestal het scherm) als naar een of meerdere bestanden. Dit is handig wanneer je de uitvoer van een commando wilt bekijken en tegelijkertijd wilt opslaan.

## Gebruik
De basis syntaxis van de `tee`-opdracht is als volgt:

```bash
tee [opties] [bestanden]
```

## Veelvoorkomende Opties
- `-a`, `--append`: Voeg de uitvoer toe aan het einde van het opgegeven bestand in plaats van het bestand te overschrijven.
- `-i`, `--ignore-interrupts`: Negeer onderbrekingen (zoals Ctrl+C).
- `--help`: Toon een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toon de versie-informatie van de `tee`-opdracht.

## Veelvoorkomende Voorbeelden

1. **Basisgebruik**: Schrijf de uitvoer van een commando naar een bestand.
   ```bash
   echo "Hallo, wereld!" | tee bestand.txt
   ```

2. **Meerdere bestanden**: Schrijf de uitvoer naar meerdere bestanden.
   ```bash
   echo "Dit is een test." | tee bestand1.txt bestand2.txt
   ```

3. **Toevoegen aan een bestand**: Voeg uitvoer toe aan een bestaand bestand zonder het te overschrijven.
   ```bash
   echo "Nieuwe regel." | tee -a bestand.txt
   ```

4. **Gebruik met andere commando's**: Combineer `tee` met andere commando's, zoals `grep`.
   ```bash
   dmesg | grep "fout" | tee fouten.txt
   ```

## Tips
- Gebruik `tee` in een pijplijn om de uitvoer van een commando te bekijken terwijl je deze opslaat.
- Wees voorzichtig met het overschrijven van bestanden; gebruik de `-a` optie als je wilt toevoegen in plaats van overschrijven.
- Combineer `tee` met `sudo` als je uitvoer naar een bestand wilt schrijven waarvoor root-toegang vereist is, bijvoorbeeld:
  ```bash
  echo "Configuratie toegevoegd" | sudo tee /etc/config.txt
  ```