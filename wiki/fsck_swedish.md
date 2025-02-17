# [Linux] Bash fsck användning: Kontrollera och reparera filsystem

## Översikt
`fsck` (file system check) är ett verktyg i Unix-liknande operativsystem som används för att kontrollera och reparera filsystem. Det säkerställer att filsystemet är i ett konsekvent tillstånd och kan åtgärda eventuella fel som upptäckts.

## Användning
Den grundläggande syntaxen för `fsck` är:

```bash
fsck [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Automatisk reparation av fel utan att be om bekräftelse.
- `-n`: Utför en kontroll utan att göra några ändringar.
- `-y`: Svara "ja" på alla frågor under reparationen.
- `-t`: Specifiera en typ av filsystem att kontrollera.
- `-f`: Tvinga en kontroll även om filsystemet verkar vara rent.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `fsck`:

1. Kontrollera ett specifikt filsystem:
   ```bash
   fsck /dev/sda1
   ```

2. Automatisk reparation av ett filsystem:
   ```bash
   fsck -a /dev/sda1
   ```

3. Kontrollera ett filsystem utan att göra några ändringar:
   ```bash
   fsck -n /dev/sda1
   ```

4. Tvinga en kontroll av ett filsystem:
   ```bash
   fsck -f /dev/sda1
   ```

5. Svara "ja" på alla frågor under reparation:
   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Använd `fsck` på avmonterade filsystem för att undvika dataförlust.
- Kontrollera alltid filsystemet efter en oväntad nedstängning eller strömavbrott.
- Var försiktig med alternativet `-y`, eftersom det kan leda till oönskade ändringar utan bekräftelse.