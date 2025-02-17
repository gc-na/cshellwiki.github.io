# [Linux] Bash stty användning: Konfigurera terminalinställningar

## Översikt
`stty` är ett kommandoradsverktyg i Unix-liknande operativsystem som används för att ändra och visa terminalinställningar. Det kan justera hur terminalen hanterar in- och utdata, vilket gör det möjligt att anpassa användarens interaktion med terminalen.

## Användning
Den grundläggande syntaxen för `stty` är:

```bash
stty [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar alla aktuella inställningar för terminalen.
- `-g`: Visar inställningarna i en form som kan användas för att återställa dem senare.
- `erase`: Ställer in tecknet som används för att ta bort det föregående tecknet.
- `kill`: Ställer in tecknet som används för att radera hela raden.
- `intr`: Ställer in tecknet för att avbryta en process.

## Vanliga exempel
Här är några praktiska exempel på hur `stty` kan användas:

### Visa aktuella inställningar
För att visa alla aktuella terminalinställningar kan du använda:

```bash
stty -a
```

### Ändra raderings-tecknet
Om du vill ändra raderings-tecknet till `^H` (backspace) kan du använda:

```bash
stty erase ^H
```

### Ställ in avbrytstecken
För att ställa in avbrytstecknet till `Ctrl+C`, kan du använda:

```bash
stty intr ^C
```

### Spara och återställ inställningar
För att spara de aktuella inställningarna kan du använda:

```bash
stty -g > stty_settings.txt
```

Och för att återställa dem senare:

```bash
stty $(< stty_settings.txt)
```

## Tips
- Kontrollera alltid dina terminalinställningar efter att ha kört kommandon som kan påverka dem.
- Använd `stty -g` för att spara inställningar innan du gör ändringar, så att du kan återställa dem vid behov.
- Var försiktig när du ändrar inställningar, eftersom felaktiga inställningar kan påverka hur du interagerar med terminalen.