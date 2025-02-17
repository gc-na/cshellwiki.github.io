# [Linux] Bash cal användning: Visa kalendrar

## Översikt
`cal` är ett kommandoradsverktyg som används för att visa kalendrar i terminalen. Det kan visa en månad eller ett helt år och ger en snabb översikt över datum och veckodagar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
cal [alternativ] [argument]
```

## Vanliga alternativ
- `-m`: Visa månadens namn på engelska.
- `-y`: Visa hela året.
- `-3`: Visa den aktuella månaden, föregående månad och nästa månad.
- `-j`: Visa dagen i året (Julian datum).
- `-A [n]`: Visa n månader framåt.
- `-B [n]`: Visa n månader bakåt.

## Vanliga exempel
Visa den aktuella månaden:

```bash
cal
```

Visa en specifik månad och år (t.ex. februari 2023):

```bash
cal 02 2023
```

Visa hela året 2023:

```bash
cal -y 2023
```

Visa den aktuella månaden samt föregående och nästa månad:

```bash
cal -3
```

Visa kalendern med julian datum:

```bash
cal -j
```

Visa kalendern för de kommande 3 månaderna:

```bash
cal -A 3
```

## Tips
- Använd `cal -m` för att få månadsnamn på engelska, vilket kan vara användbart om du arbetar i en internationell miljö.
- Kombinera alternativ för att anpassa visningen, till exempel `cal -A 1 -B 1` för att se en månad före och efter den aktuella månaden.
- För att snabbt få en översikt över viktiga datum, kan du använda `cal` tillsammans med andra kommandon i skript för att automatisera rapportering av händelser.