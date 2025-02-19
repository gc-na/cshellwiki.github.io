# [Linux] C Shell (csh) vigr gebruik: Bewerken van het /etc/hosts-bestand

## Overzicht
De `vigr`-opdracht wordt gebruikt om het `/etc/passwd`-bestand en het `/etc/group`-bestand veilig te bewerken. Het opent deze bestanden in een teksteditor, waarbij het ervoor zorgt dat de bestandsintegriteit behouden blijft tijdens het bewerken.

## Gebruik
De basis syntaxis van de `vigr`-opdracht is als volgt:

```csh
vigr [opties] [bestanden]
```

## Veelvoorkomende Opties
- `-s`: Voer de opdracht uit in een stille modus, zonder extra uitvoer.
- `-f`: Specificeer een ander bestand dan de standaard `/etc/passwd` of `/etc/group`.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `vigr`-opdracht:

1. **Bewerken van het passwd-bestand**:
   ```csh
   vigr
   ```

2. **Bewerken van het group-bestand**:
   ```csh
   vigr -f /etc/group
   ```

3. **Bewerken van een specifiek passwd-bestand**:
   ```csh
   vigr -f /path/to/custom_passwd
   ```

## Tips
- Zorg ervoor dat je voldoende rechten hebt om de bestanden te bewerken, meestal zijn root-rechten vereist.
- Gebruik de `-s` optie als je geen extra uitvoer wilt zien tijdens het bewerken.
- Maak altijd een back-up van belangrijke configuratiebestanden voordat je wijzigingen aanbrengt.