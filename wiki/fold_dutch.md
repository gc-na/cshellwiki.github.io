# [Linux] Bash fold gebruik: Tekstregels afbreken

## Overzicht
De `fold`-opdracht in Bash wordt gebruikt om lange tekstregels af te breken in kortere regels. Dit is vooral handig voor het weergeven van tekst op terminals met beperkte breedte of voor het voorbereiden van tekstbestanden voor afdrukken.

## Gebruik
De basis syntaxis van de `fold`-opdracht is als volgt:

```bash
fold [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-w, --width`: Bepaalt de maximale breedte van de regels. Standaard is dit 80 tekens.
- `-s, --spaces`: Breekt de regels af op spaties in plaats van midden in een woord.
- `-b, --bytes`: Behandelt de invoer als bytes in plaats van als tekens.

## Veelvoorkomende Voorbeelden

1. **Basis gebruik van fold**:
   Om een tekstbestand af te breken naar standaard 80 tekens:
   ```bash
   fold tekstbestand.txt
   ```

2. **Afbreken met specifieke breedte**:
   Om een tekstbestand af te breken naar 50 tekens:
   ```bash
   fold -w 50 tekstbestand.txt
   ```

3. **Afbreken op spaties**:
   Om een tekstbestand af te breken op spaties:
   ```bash
   fold -s -w 50 tekstbestand.txt
   ```

4. **Afbreken van invoer vanuit een pipe**:
   Je kunt `fold` ook gebruiken met een pipe om de uitvoer van een andere opdracht af te breken:
   ```bash
   echo "Dit is een lange zin die we willen afbreken." | fold -w 20
   ```

## Tips
- Gebruik de `-s` optie als je wilt dat woorden niet worden afgebroken, wat de leesbaarheid kan verbeteren.
- Experimenteer met verschillende breedtes om te zien wat het beste werkt voor jouw specifieke situatie.
- Combineer `fold` met andere tekstverwerkingsopdrachten zoals `cat` of `grep` voor meer complexe bewerkingen.