# [Linux] Bash fsck gebruik: Controleer en repareer bestandssystemen

## Overzicht
De `fsck` (file system check) opdracht wordt gebruikt om de integriteit van bestandssystemen te controleren en eventuele fouten te repareren. Het is een essentieel hulpmiddel voor systeembeheerders om ervoor te zorgen dat schijven en partities correct functioneren.

## Gebruik
De basis syntaxis van de `fsck` opdracht is als volgt:

```bash
fsck [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a` : Probeert automatisch fouten te repareren zonder gebruikersinteractie.
- `-n` : Voert een controle uit zonder wijzigingen aan te brengen (alleen lezen).
- `-y` : Bevestigt automatisch alle reparaties.
- `-t` : Geeft het type bestandssysteem op dat gecontroleerd moet worden.
- `-f` : Dwingt een controle af, zelfs als het bestandssysteem als schoon wordt gemarkeerd.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `fsck`:

1. Controleer een specifiek bestandssysteem:
   ```bash
   fsck /dev/sda1
   ```

2. Voer een automatische reparatie uit:
   ```bash
   fsck -a /dev/sda1
   ```

3. Controleer zonder wijzigingen aan te brengen:
   ```bash
   fsck -n /dev/sda1
   ```

4. Bevestig automatisch alle reparaties:
   ```bash
   fsck -y /dev/sda1
   ```

5. Controleer een ext4 bestandssysteem:
   ```bash
   fsck.ext4 /dev/sda1
   ```

## Tips
- Voer `fsck` altijd uit wanneer het bestandssysteem niet gemount is om gegevensverlies te voorkomen.
- Maak regelmatig back-ups van belangrijke gegevens voordat je `fsck` gebruikt, vooral bij het repareren van fouten.
- Gebruik de `-n` optie om een controle uit te voeren zonder wijzigingen aan te brengen, zodat je kunt zien welke fouten er zijn voordat je actie onderneemt.