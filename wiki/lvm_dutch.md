# [Linux] Bash lvm gebruik: Beheer van logische volumes

## Overzicht
De `lvm` (Logical Volume Manager) command is een krachtige tool voor het beheren van opslag op Linux-systemen. Het stelt gebruikers in staat om logische volumes te creëren, te verwijderen en te beheren, wat flexibiliteit biedt in het gebruik van schijfruimte.

## Gebruik
De basis syntaxis van de `lvm` command is als volgt:

```bash
lvm [opties] [argumenten]
```

## Veelvoorkomende opties
- `create`: Maak een nieuw logisch volume aan.
- `remove`: Verwijder een logisch volume.
- `extend`: Breid een bestaand logisch volume uit.
- `reduce`: Verminder de grootte van een logisch volume.
- `list`: Toon een lijst van beschikbare logische volumes.

## Veelvoorkomende voorbeelden

### 1. Een logisch volume aanmaken
Om een nieuw logisch volume aan te maken, gebruik je de volgende opdracht:

```bash
lvm create -n mijn_volume -L 10G mijn_volume_group
```

### 2. Een logisch volume verwijderen
Om een logisch volume te verwijderen, gebruik je deze opdracht:

```bash
lvm remove mijn_volume
```

### 3. Een logisch volume uitbreiden
Om een logisch volume uit te breiden met 5G, gebruik je:

```bash
lvm extend -L +5G mijn_volume
```

### 4. Een logisch volume verkleinen
Om een logisch volume te verkleinen, gebruik je:

```bash
lvm reduce -L -5G mijn_volume
```

### 5. Een lijst van logische volumes weergeven
Om een lijst van alle logische volumes te bekijken, gebruik je:

```bash
lvm list
```

## Tips
- Zorg ervoor dat je altijd een back-up hebt van belangrijke gegevens voordat je wijzigingen aanbrengt aan logische volumes.
- Gebruik de `--dry-run` optie om te zien wat er zou gebeuren zonder daadwerkelijk wijzigingen aan te brengen.
- Houd rekening met de filesystem-grootte bij het verkleinen van logische volumes; zorg ervoor dat je de filesystem eerst verkleint voordat je het volume zelf verkleint.