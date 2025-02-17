# [Linux] Bash lvs användning: Visa logiska volymer

## Översikt
Kommandot `lvs` används för att visa information om logiska volymer i Linux-system som använder Logical Volume Manager (LVM). Det ger en översikt över de logiska volymer som finns på systemet, inklusive deras storlek och status.

## Användning
Den grundläggande syntaxen för kommandot `lvs` är:

```bash
lvs [alternativ] [argument]
```

## Vanliga alternativ
- `-o, --units`: Anger enhet för storlekar (t.ex. kB, MB, GB).
- `-a, --all`: Visar även inaktiva logiska volymer.
- `-f, --full`: Visar fullständig information om logiska volymer.
- `-n, --noheading`: Visar resultat utan rubriker.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `lvs`:

1. Visa en lista över alla logiska volymer:
   ```bash
   lvs
   ```

2. Visa logiska volymer med storlekar i megabyte:
   ```bash
   lvs -o +size --units m
   ```

3. Visa även inaktiva logiska volymer:
   ```bash
   lvs -a
   ```

4. Visa fullständig information om logiska volymer:
   ```bash
   lvs -f
   ```

5. Visa logiska volymer utan rubriker:
   ```bash
   lvs -n
   ```

## Tips
- Använd `lvs` tillsammans med andra LVM-kommandon som `lvcreate` och `lvremove` för att hantera logiska volymer effektivt.
- För att få en mer detaljerad översikt, överväg att kombinera `lvs` med `grep` för att filtrera resultaten.
- Kontrollera regelbundet statusen för dina logiska volymer för att säkerställa att de fungerar som de ska.