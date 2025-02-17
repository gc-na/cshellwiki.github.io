# [Linux] Bash write användning: Skicka meddelanden till användare

## Översikt
Kommandot `write` används för att skicka meddelanden direkt till en annan användares terminalsession. Det är ett enkelt sätt att kommunicera med andra användare på samma system.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
write [användarnamn] [terminal]
```

Om terminalen inte anges, kommer `write` automatiskt att försöka skicka meddelandet till användarens aktiva terminal.

## Vanliga alternativ
- `-n`: Skicka meddelandet utan att vänta på att mottagaren ska läsa det.
- `-s`: Skicka ett kort meddelande utan att visa användarnamnet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `write`:

1. Skicka ett meddelande till en användare som heter "anna":
   ```bash
   write anna
   Hej Anna, kan du kolla på filen jag skickade?
   ```

2. Skicka ett meddelande till en specifik terminal, till exempel `pts/1`:
   ```bash
   write anna pts/1
   Jag är klar med projektet, kolla gärna!
   ```

3. Använda alternativet `-s` för att skicka ett kort meddelande:
   ```bash
   write -s anna
   Vi ses snart!
   ```

## Tips
- Kontrollera att mottagaren är inloggad och har en aktiv terminal innan du skickar ett meddelande.
- Använd `who`-kommandot för att se vilka användare som är inloggade och deras terminaler.
- Tänk på att `write` inte fungerar om mottagaren har inaktiverat meddelanden med kommandot `mesg n`.