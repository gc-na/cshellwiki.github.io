# [Linux] Bash true användning: Alltid framgång

## Översikt
Kommandot `true` i Bash är en enkel och användbar funktion som alltid returnerar en framgångsstatus (exit status 0). Det används ofta i skript och kommandokedjor för att indikera att en operation har lyckats, oavsett vad som faktiskt har hänt.

## Användning
Den grundläggande syntaxen för kommandot `true` är:

```bash
true [alternativ] [argument]
```

## Vanliga alternativ
`true` har inga specifika alternativ eller argument, eftersom dess enda funktion är att returnera en framgångsstatus. 

## Vanliga exempel
Här är några praktiska exempel på hur `true` kan användas:

1. **Enkel användning i terminalen:**
   ```bash
   true
   ```
   Detta kommando körs och returnerar en framgångsstatus.

2. **Använda i en if-sats:**
   ```bash
   if true; then
       echo "Detta kommer alltid att skrivas ut."
   fi
   ```
   Eftersom `true` alltid returnerar 0, kommer meddelandet alltid att skrivas ut.

3. **Använda i en while-loop:**
   ```bash
   while true; do
       echo "Denna loop kommer att köras oändligt."
       sleep 1
   done
   ```
   Denna loop kommer att fortsätta köra tills den stoppas manuellt.

4. **Som en platsinnehavare i skript:**
   ```bash
   # TODO: Implementera funktionalitet senare
   true
   ```
   Här används `true` som en platsinnehavare för att markera att något ska implementeras senare.

## Tips
- Använd `true` i skript för att skapa dummy-kommandon där du behöver en framgångsstatus utan att utföra någon faktisk operation.
- Det kan vara användbart i kombination med andra kommandon för att säkerställa att en kedja av kommandon fortsätter att köras.
- Tänk på att `true` inte gör något annat än att returnera en framgångsstatus, så använd det endast när det är nödvändigt för logikflödet i ditt skript.