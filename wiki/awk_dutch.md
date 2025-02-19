# [Linux] C Shell (csh) awk gebruik: tekstverwerking en patroonherkenning

## Overzicht
De `awk`-opdracht is een krachtige tekstverwerkings- en patroonherkenningstool die veel wordt gebruikt in de Unix- en Linux-omgevingen. Het stelt gebruikers in staat om gegevens uit tekstbestanden te extraheren, te manipuleren en te rapporteren op basis van specifieke patronen en voorwaarden.

## Gebruik
De basis syntaxis van de `awk`-opdracht is als volgt:

```bash
awk [opties] [argumenten]
```

## Veelvoorkomende opties
- `-F`: Specificeert de veldscheidingsteken (bijvoorbeeld `-F,` voor komma's).
- `-v`: Stelt een variabele in met een waarde (bijvoorbeeld `-v var=waarde`).
- `-f`: Voert een awk-script uit dat in een bestand is opgeslagen (bijvoorbeeld `-f script.awk`).

## Veelvoorkomende voorbeelden

1. **Basis tekstverwerking**: Het afdrukken van de eerste kolom van een bestand.
   ```bash
   awk '{print $1}' bestand.txt
   ```

2. **Gebruik van een veldscheidingsteken**: Het afdrukken van de tweede kolom van een CSV-bestand.
   ```bash
   awk -F, '{print $2}' gegevens.csv
   ```

3. **Voorwaarden toepassen**: Het afdrukken van regels waar de waarde in de derde kolom groter is dan 100.
   ```bash
   awk '$3 > 100' bestand.txt
   ```

4. **Variabelen gebruiken**: Het tellen van het aantal regels in een bestand.
   ```bash
   awk 'END {print NR}' bestand.txt
   ```

5. **Gecombineerde acties**: Het afdrukken van de eerste en derde kolom, gescheiden door een koppelteken.
   ```bash
   awk '{print $1 "-" $3}' bestand.txt
   ```

## Tips
- Gebruik `-F` om het juiste scheidingsteken in te stellen voor uw gegevens.
- Probeer uw `awk`-scripts te scheiden in bestanden voor complexere bewerkingen, wat de leesbaarheid vergroot.
- Maak gebruik van de `BEGIN` en `END` blokken om initiële instellingen en eindresultaten te beheren.