# [Linux] Bash killall användning: Avsluta processer baserat på namn

## Översikt
Kommandot `killall` används för att avsluta alla processer med ett specifikt namn. Det är ett kraftfullt verktyg för att hantera processer i Unix-liknande operativsystem, vilket gör det möjligt att snabbt stänga ner program som körs i bakgrunden.

## Användning
Den grundläggande syntaxen för `killall` ser ut så här:

```
killall [alternativ] [argument]
```

## Vanliga alternativ
- `-u, --user <användare>`: Avsluta processer som tillhör en specifik användare.
- `-i, --interactive`: Bekräfta innan varje process avslutas.
- `-v, --verbose`: Visa detaljerad information om vilka processer som avslutas.
- `-s, --signal <signal>`: Specificera vilken signal som ska skickas till processerna (standard är SIGTERM).

## Vanliga exempel
Här är några praktiska exempel på hur man använder `killall`:

1. Avsluta alla processer med namnet "firefox":
   ```bash
   killall firefox
   ```

2. Avsluta alla processer med namnet "gedit" och be om bekräftelse:
   ```bash
   killall -i gedit
   ```

3. Avsluta alla processer som tillhör användaren "john":
   ```bash
   killall -u john
   ```

4. Skicka en specifik signal (t.ex. SIGKILL) till alla processer med namnet "myapp":
   ```bash
   killall -s SIGKILL myapp
   ```

## Tips
- Använd `killall -v` för att få mer information om vilka processer som avslutas, vilket kan vara användbart för felsökning.
- Var försiktig när du använder `killall`, särskilt med kraftfulla signaler som SIGKILL, eftersom det kan leda till dataförlust om processerna inte får möjlighet att stänga ner ordentligt.
- Om du är osäker på vilka processer som kommer att avslutas, kan du först använda kommandot `pgrep` för att lista processerna innan du använder `killall`.