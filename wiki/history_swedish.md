# [Linux] Bash-historik användning: Visa och hantera kommandon

## Översikt
`history`-kommandot används för att visa en lista över tidigare körda kommandon i Bash-skalet. Det är ett användbart verktyg för att snabbt återanvända kommandon utan att behöva skriva dem på nytt.

## Användning
Den grundläggande syntaxen för `history`-kommandot är:

```
history [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Rensar hela kommandolistan.
- `-d [nummer]`: Tar bort det angivna kommandot från historiken.
- `n`: Visar de senaste `n` kommandona.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `history`-kommandot:

1. Visa hela kommandohistoriken:
   ```bash
   history
   ```

2. Visa de senaste 10 kommandona:
   ```bash
   history 10
   ```

3. Rensa hela kommandohistoriken:
   ```bash
   history -c
   ```

4. Ta bort ett specifikt kommando (t.ex. nummer 5):
   ```bash
   history -d 5
   ```

5. Återanvänd ett kommando från historiken (t.ex. nummer 3):
   ```bash
   !3
   ```

## Tips
- Använd `Ctrl + R` för att söka i din kommandohistorik interaktivt.
- Kombinera `history` med `grep` för att snabbt hitta specifika kommandon, till exempel:
  ```bash
  history | grep "git"
  ```
- Kom ihåg att historiken kan vara begränsad av inställningar i din Bash-konfiguration, så kontrollera `HISTSIZE` och `HISTFILESIZE` om du vill ändra dessa värden.