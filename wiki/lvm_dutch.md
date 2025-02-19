# [Linux] C Shell (csh) lvm gebruik: Beheer van logische volumes

## Overzicht
De `lvm` (Logical Volume Manager) commandoregeltool wordt gebruikt voor het beheren van logische volumes in Linux-systemen. Het stelt gebruikers in staat om opslagruimten flexibeler te beheren door volumes te creëren, te verwijderen, te vergroten of te verkleinen.

## Gebruik
De basis syntaxis van de `lvm` commandoregel is als volgt:

```csh
lvm [opties] [argumenten]
```

## Veelvoorkomende Opties
- `create`: Maak een nieuw logisch volume aan.
- `remove`: Verwijder een logisch volume.
- `extend`: Vergroot een bestaand logisch volume.
- `reduce`: Verklein een bestaand logisch volume.
- `list`: Toon een lijst van alle beschikbare logische volumes.

## Veelvoorkomende Voorbeelden

### Een nieuw logisch volume maken
```csh
lvm create my_volume --size 10G --name my_logical_volume
```

### Een logisch volume verwijderen
```csh
lvm remove my_logical_volume
```

### Een logisch volume vergroten
```csh
lvm extend my_logical_volume --size +5G
```

### Een logisch volume verkleinen
```csh
lvm reduce my_logical_volume --size -2G
```

### Lijst van logische volumes weergeven
```csh
lvm list
```

## Tips
- Zorg ervoor dat je altijd een back-up hebt van belangrijke gegevens voordat je wijzigingen aanbrengt in logische volumes.
- Gebruik de `--dry-run` optie om te zien wat er zou gebeuren zonder daadwerkelijk wijzigingen aan te brengen.
- Controleer regelmatig de status van je logische volumes om problemen vroegtijdig te signaleren.