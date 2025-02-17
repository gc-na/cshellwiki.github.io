# [Linux] Bash fc användning: Hantera och redigera kommandon i historiken

## Översikt
`fc`-kommandot används för att visa, redigera och återanvända tidigare kommandon från Bash-historiken. Det är ett kraftfullt verktyg för att snabbt korrigera eller modifiera tidigare utförda kommandon.

## Användning
Den grundläggande syntaxen för `fc`-kommandot är:

```bash
fc [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Lista kommandon från historiken.
- `-r`: Lista kommandon i omvänd ordning.
- `-s`: Utför ett kommando direkt utan att öppna en redigerare.
- `-n`: Visa inte radnummer i listan.

## Vanliga exempel
### Lista de senaste kommandona
För att lista de senaste 10 kommandona i historiken kan du använda:

```bash
fc -l -n -10
```

### Redigera ett specifikt kommando
Om du vill redigera ett kommando med ett specifikt nummer (t.ex. nummer 42):

```bash
fc 42
```

### Utför ett kommando direkt
För att snabbt återanvända det senaste kommandot utan att redigera det:

```bash
fc -s
```

### Lista kommandon i omvänd ordning
För att se de senaste kommandona i omvänd ordning:

```bash
fc -r -l 10
```

## Tips
- Använd `fc` för att snabbt korrigera fel i tidigare kommandon utan att behöva skriva om dem.
- Du kan kombinera `fc` med andra kommandon för att skapa effektiva arbetsflöden.
- Kom ihåg att `fc` öppnar den standardredigerare som är inställd i din miljö, så se till att du är bekväm med den redigeraren.