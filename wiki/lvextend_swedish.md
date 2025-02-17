# [Linux] Bash lvextend användning: Utöka logiska volymer

## Översikt
Kommandot `lvextend` används för att öka storleken på en logisk volym i Linux. Detta är en viktig funktion när du behöver mer utrymme på en befintlig volym utan att behöva skapa en ny.

## Användning
Den grundläggande syntaxen för kommandot `lvextend` är:

```bash
lvextend [alternativ] [argument]
```

## Vanliga alternativ
- `-L +[storlek]`: Öka storleken med den angivna storleken.
- `-l +[antal]`: Öka storleken med det angivna antalet logiska enheter.
- `-r`: Reskalera filsystemet automatiskt efter att volymen har utökats.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `lvextend`:

1. **Öka storleken på en logisk volym med 10 GB:**
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Öka storleken på en logisk volym med 5 logiska enheter:**
   ```bash
   lvextend -l +5 /dev/vg01/lv01
   ```

3. **Öka storleken och reskalera filsystemet automatiskt:**
   ```bash
   lvextend -r -L +20G /dev/vg01/lv01
   ```

## Tips
- Kontrollera alltid den aktuella storleken på din logiska volym innan du gör ändringar med kommandot `lvdisplay`.
- Använd alternativet `-r` för att spara tid och undvika att behöva reskalera filsystemet manuellt efter att ha utökat volymen.
- Se till att du har tillräckligt med ledigt utrymme i den underliggande volymgruppen innan du försöker utöka en logisk volym.