# [Linux] Bash split användning: Dela upp filer i mindre delar

## Översikt
Kommandot `split` används för att dela upp stora filer i mindre delar. Detta kan vara användbart för att hantera stora datamängder eller för att överföra filer som har storlekbegränsningar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
split [alternativ] [argument]
```

## Vanliga alternativ
- `-l [antal]`: Dela filen efter ett visst antal rader.
- `-b [storlek]`: Dela filen efter en viss storlek (t.ex. `100k` för 100 kilobyte).
- `-d`: Använd siffror istället för bokstäver för att namnge de delade filerna.
- `--additional-suffix=[suffix]`: Lägg till ett suffix till de delade filerna.

## Vanliga exempel
Dela en fil i delar om 100 rader:

```bash
split -l 100 storfil.txt
```

Dela en fil i delar om 1 megabyte:

```bash
split -b 1M storfil.txt
```

Dela en fil och använd siffror för namnen:

```bash
split -d -l 50 storfil.txt deladfil_
```

Dela en fil och lägg till ett suffix:

```bash
split --additional-suffix=.txt -b 500k storfil.txt deladfil_
```

## Tips
- Kontrollera storleken på de delade filerna efter att du har använt `split` för att säkerställa att de är i önskad storlek.
- Använd `cat` för att sammanfoga de delade filerna igen om det behövs.
- Var medveten om att `split` inte bevarar filens metadata, så om det är viktigt, se till att notera det innan du delar filen.