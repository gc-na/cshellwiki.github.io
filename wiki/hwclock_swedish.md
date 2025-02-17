# [Linux] Bash hwclock användning: Hantera systemklockan

## Översikt
Kommandot `hwclock` används för att läsa och ställa in hårdvaruklockan på en dator. Hårdvaruklockan, även känd som RTC (Real-Time Clock), är en klocka som fortsätter att hålla tid även när datorn är avstängd.

## Användning
Den grundläggande syntaxen för kommandot är:

```
hwclock [alternativ] [argument]
```

## Vanliga alternativ
- `--show`: Visar den aktuella tiden från hårdvaruklockan.
- `--set`: Ställer in hårdvaruklockan till den angivna tiden.
- `--systohc`: Ställer in hårdvaruklockan till systemets aktuella tid.
- `--hctosys`: Ställer in systemets tid till hårdvaruklockans tid.
- `--utc`: Anger att tiden ska tolkas som UTC (Coordinated Universal Time).

## Vanliga exempel
Här är några praktiska exempel på hur man använder `hwclock`:

1. Visa den aktuella tiden från hårdvaruklockan:
   ```bash
   hwclock --show
   ```

2. Ställ in hårdvaruklockan till en specifik tid:
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. Ställ in hårdvaruklockan till systemets aktuella tid:
   ```bash
   hwclock --systohc
   ```

4. Ställ in systemets tid till hårdvaruklockans tid:
   ```bash
   hwclock --hctosys
   ```

5. Visa tiden i UTC-format:
   ```bash
   hwclock --show --utc
   ```

## Tips
- Kontrollera alltid att systemets tid är korrekt innan du ställer in hårdvaruklockan.
- Använd `--utc` om du arbetar med flera operativsystem som kan använda olika tidszoner.
- Det kan vara bra att köra `hwclock` med root-privilegier för att säkerställa att du har tillgång till att ställa in klockan.