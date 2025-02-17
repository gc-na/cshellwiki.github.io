# [Linux] Bash fg användning: Återställ en bakgrundsprocess till förgrunden

## Översikt
`fg`-kommandot används för att återställa en bakgrundsprocess till förgrunden i en terminalsession. Detta gör att du kan interagera med processen direkt, vilket är användbart när du behöver ge den fokus eller när den kräver användarinmatning.

## Användning
Den grundläggande syntaxen för `fg`-kommandot är:

```
fg [alternativ] [argument]
```

## Vanliga alternativ
- **%jobnummer**: Anger vilket jobb som ska återställas till förgrunden. Jobbnumret kan anges med ett procenttecken följt av jobbnummret (t.ex. `%1`).
- **-l**: Visar en lista över alla jobb som körs i bakgrunden.

## Vanliga exempel
Här är några praktiska exempel på hur `fg` kan användas:

1. Återställ det senaste bakgrundsarbetet till förgrunden:
   ```bash
   fg
   ```

2. Återställ ett specifikt jobb (t.ex. jobb nummer 1):
   ```bash
   fg %1
   ```

3. Lista alla bakgrundsjobb:
   ```bash
   jobs -l
   ```

4. Återställ ett jobb med ett specifikt namn (om det är angivet):
   ```bash
   fg %job_name
   ```

## Tips
- Använd `jobs`-kommandot för att se en lista över aktiva bakgrundsjobb innan du använder `fg`.
- Om du har flera bakgrundsjobb, kom ihåg att ange rätt jobbnummret för att undvika förvirring.
- Tänk på att `fg` bara fungerar i den aktuella terminalsessionen; om du öppnar en ny terminal kommer du inte att kunna återställa bakgrundsjobb från en annan session.