# [Linux] Bash nl gebruik: nummeren van regels in tekstbestanden

## Overzicht
De `nl` opdracht in Bash wordt gebruikt om de regels van een tekstbestand te nummeren. Dit is handig voor het maken van genummerde lijsten of voor het analyseren van bestanden waar regelnummering nuttig kan zijn.

## Gebruik
De basis syntaxis van de `nl` opdracht is als volgt:

```bash
nl [opties] [argumenten]
```

## Veelvoorkomende opties
- `-b`: Bepaalt welke regels genummerd moeten worden. Bijvoorbeeld, `-b a` nummer alle regels, terwijl `-b t` alleen de niet-lege regels nummer.
- `-f`: Hiermee kun je het nummeren van regels in een nieuw bestand starten na een bepaalde regel.
- `-n`: Bepaalt het nummeringsformaat. Bijvoorbeeld, `-n ln` voor links uitgelijnde nummers, `-n rn` voor rechts uitgelijnde nummers, en `-n rz` voor cijfers met voorloopnullen.
- `-w`: Hiermee kun je de breedte van de nummering instellen.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basis nummering
Nummer de regels van een bestand genaamd `voorbeeld.txt`:

```bash
nl voorbeeld.txt
```

### Voorbeeld 2: Alleen niet-lege regels nummeren
Nummer alleen de niet-lege regels in `voorbeeld.txt`:

```bash
nl -b t voorbeeld.txt
```

### Voorbeeld 3: Specifiek nummeringsformaat
Nummer de regels met rechts uitgelijnde nummers:

```bash
nl -n rn voorbeeld.txt
```

### Voorbeeld 4: Breedte van nummering instellen
Stel de breedte van de nummering in op 5 karakters:

```bash
nl -w 5 voorbeeld.txt
```

## Tips
- Gebruik de `-b` optie om te bepalen welke regels je wilt nummeren, afhankelijk van je behoeften.
- Experimenteer met de `-n` optie om te zien welk nummeringsformaat het beste bij je document past.
- Combineer opties voor meer geavanceerde nummering, zoals het nummeren van alleen bepaalde secties van een bestand.