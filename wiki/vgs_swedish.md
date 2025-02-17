# [Linux] Bash vgs användning: Visa information om volygrupper

## Översikt
Kommandot `vgs` används för att visa information om volygrupper i Linux-system som använder Logical Volume Manager (LVM). Det ger en snabb översikt över volygrupper, inklusive deras storlek, tillgängligt utrymme och andra viktiga attribut.

## Användning
Den grundläggande syntaxen för kommandot `vgs` är:

```
vgs [alternativ] [argument]
```

## Vanliga alternativ
- `-o, --units`: Specificera enhet för utdata, till exempel kB, MB, GB.
- `--noheadings`: Visa inte rubriker i utdata.
- `-a, --all`: Visa alla volygrupper, inklusive inaktiva.
- `-h, --help`: Visa hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `vgs`:

1. Visa grundläggande information om alla volygrupper:
   ```bash
   vgs
   ```

2. Visa information om en specifik volygrupp:
   ```bash
   vgs vg01
   ```

3. Visa information utan rubriker:
   ```bash
   vgs --noheadings
   ```

4. Visa information med specifika enheter (t.ex. GB):
   ```bash
   vgs -o +vg_size,vg_free --units g
   ```

5. Visa även inaktiva volygrupper:
   ```bash
   vgs --all
   ```

## Tips
- Använd `vgs` tillsammans med andra LVM-kommandon som `lvdisplay` och `pvdisplay` för att få en mer omfattande bild av din lagringskonfiguration.
- För att snabbt få en översikt över tillgängligt utrymme, använd alternativet `-o` för att specificera vilka fält som ska visas.
- Kom ihåg att köra `vgs` med sudo om du inte har tillräckliga rättigheter för att se volygruppsinformation.