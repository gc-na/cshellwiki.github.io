# [Linux] Bash printf användning: Formaterad utskrift av text

## Översikt
`printf`-kommandot används för att formatera och skriva ut text till standardutgången. Det är kraftfullt och flexibelt, vilket gör det möjligt att styra hur data presenteras, inklusive justering, decimaler och specialtecken.

## Användning
Den grundläggande syntaxen för `printf` är:

```bash
printf [alternativ] [argument]
```

## Vanliga alternativ
- `-v`: Spara resultatet i en variabel.
- `%s`: Formaterar en sträng.
- `%d`: Formaterar ett heltal.
- `%f`: Formaterar ett flyttal.
- `%x`: Formaterar ett heltal som hexadecimalt.

## Vanliga exempel

### Exempel 1: Enkel utskrift av en sträng
```bash
printf "Hej, världen!\n"
```

### Exempel 2: Formatering av ett heltal
```bash
printf "Numret är: %d\n" 42
```

### Exempel 3: Utskrift av flyttal med decimaler
```bash
printf "Pi är ungefär: %.2f\n" 3.14159
```

### Exempel 4: Utskrift av flera variabler
```bash
name="Alice"
age=30
printf "%s är %d år gammal.\n" "$name" "$age"
```

### Exempel 5: Använda hexadecimalt format
```bash
printf "Hexadecimalt värde: %x\n" 255
```

## Tips
- Använd `\n` för att skapa nya rader i utskriften.
- Tänk på att `printf` inte automatiskt lägger till en ny rad i slutet av utskriften, till skillnad från `echo`.
- Du kan kombinera formatsträngar för att skapa mer komplexa utskrifter, vilket gör `printf` mycket mångsidigt.