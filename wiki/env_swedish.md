# [Linux] Bash env användning: Hantera miljövariabler

## Översikt
Kommandot `env` används för att visa eller ändra miljövariabler i en Unix-liknande miljö. Det kan också användas för att köra ett program med en modifierad miljö.

## Användning
Den grundläggande syntaxen för kommandot `env` är:

```
env [alternativ] [argument]
```

## Vanliga alternativ
- `-i` : Startar en ny miljö utan några miljövariabler.
- `-u VARIABEL` : Tar bort den angivna miljövariabeln.
- `VARIABEL=VÄRDE` : Sätter en miljövariabel till ett specifikt värde innan ett kommando körs.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `env`:

1. **Visa alla miljövariabler:**
   ```bash
   env
   ```

2. **Köra ett kommando med en specifik miljövariabel:**
   ```bash
   env PATH=/usr/local/bin my_command
   ```

3. **Ta bort en miljövariabel:**
   ```bash
   env -u MY_VAR my_command
   ```

4. **Starta en ny miljö utan några miljövariabler:**
   ```bash
   env -i bash
   ```

5. **Sätta flera miljövariabler och köra ett kommando:**
   ```bash
   env VAR1=value1 VAR2=value2 my_command
   ```

## Tips
- Använd `env` för att testa hur ett program beter sig med olika miljöinställningar.
- Kombinera `env` med skript för att säkerställa att de körs med rätt miljövariabler.
- Var försiktig när du tar bort miljövariabler, eftersom det kan påverka andra program som körs i samma session.