# [Linux] Bash vgextend gebruik: Vergroot een volume groep

## Overzicht
De `vgextend` opdracht in Bash wordt gebruikt om een bestaande volume groep (VG) uit te breiden met extra fysieke volumes (PV's). Dit is handig wanneer je meer opslagruimte nodig hebt voor je logische volumes (LV's) binnen een volume groep.

## Gebruik
De basis syntaxis van de `vgextend` opdracht is als volgt:

```bash
vgextend [opties] [volume_groep] [fysieke_volumes]
```

## Veelvoorkomende Opties
- `-f`, `--force`: Dwingt de uitbreiding af, zelfs als er waarschuwingen zijn.
- `-n`, `--nosync`: Voorkomt dat de metadata van de volume groep wordt gesynchroniseerd na de uitbreiding.
- `--test`: Voert een test uit zonder daadwerkelijk wijzigingen aan te brengen.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een volume groep uitbreiden met één fysiek volume
```bash
vgextend mijn_vg /dev/sdb1
```
Dit commando voegt het fysieke volume `/dev/sdb1` toe aan de volume groep `mijn_vg`.

### Voorbeeld 2: Meerdere fysieke volumes toevoegen
```bash
vgextend mijn_vg /dev/sdb1 /dev/sdc1
```
Hiermee worden zowel `/dev/sdb1` als `/dev/sdc1` toegevoegd aan de volume groep `mijn_vg`.

### Voorbeeld 3: Uitbreiding met de force optie
```bash
vgextend -f mijn_vg /dev/sdd1
```
Dit dwingt de uitbreiding van de volume groep `mijn_vg` met het fysieke volume `/dev/sdd1`, ongeacht eventuele waarschuwingen.

## Tips
- Zorg ervoor dat de fysieke volumes die je wilt toevoegen, geconfigureerd zijn en niet in gebruik zijn door andere processen.
- Controleer altijd de status van je volume groep na de uitbreiding met het commando `vgdisplay` om te bevestigen dat de uitbreiding succesvol was.
- Maak regelmatig een back-up van je gegevens voordat je wijzigingen aanbrengt in je opslagconfiguratie.