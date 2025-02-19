# [Linux] C Shell (csh) lvcreate gebruik: Schijfvolume maken

## Overzicht
De `lvcreate` opdracht wordt gebruikt om logische volumes te maken binnen een Logical Volume Manager (LVM) op een Linux-systeem. Dit stelt gebruikers in staat om flexibele schijfpartities te beheren en aan te passen.

## Gebruik
De basis syntaxis van de `lvcreate` opdracht is als volgt:

```csh
lvcreate [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n` : Geeft de naam op voor het nieuwe logische volume.
- `-L` : Bepaalt de grootte van het logische volume.
- `-l` : Specificeert de grootte in logische eenheden (LVU).
- `-m` : Bepaalt het aantal kopieën (mirroring) van het volume.
- `-Z` : Bepaalt of het volume moet worden geactiveerd bij creatie.

## Veelvoorkomende Voorbeelden

1. **Een nieuw logische volume maken met een specifieke grootte:**
   ```csh
   lvcreate -L 10G -n mijn_volume vg01
   ```

2. **Een logische volume maken met een grootte in logische eenheden:**
   ```csh
   lvcreate -l 100 -n mijn_volume vg01
   ```

3. **Een gemirrored logische volume maken:**
   ```csh
   lvcreate -m 1 -L 20G -n gemirror_volume vg01
   ```

4. **Een logische volume maken en het direct activeren:**
   ```csh
   lvcreate -L 5G -n actief_volume -Z y vg01
   ```

## Tips
- Zorg ervoor dat je voldoende ruimte hebt op je fysieke volumes voordat je een nieuw logisch volume aanmaakt.
- Gebruik duidelijke en beschrijvende namen voor je logische volumes om verwarring te voorkomen.
- Controleer altijd de status van je volumes na creatie met de `lvdisplay` opdracht om te bevestigen dat alles correct is aangemaakt.