# [Linux] Bash shutdown användning: Stänger av eller startar om systemet

## Översikt
Kommandot `shutdown` används för att stänga av eller starta om ett Linux-system på ett kontrollerat sätt. Det tillåter användare att schemalägga avstängningar och informera andra användare om systemets status.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
shutdown [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Stänger av systemet.
- `-r`: Startar om systemet.
- `-t [tid]`: Anger en tidsfördröjning i sekunder innan avstängning eller omstart.
- `now`: Anger att avstängningen eller omstarten ska ske omedelbart.
- `+[minuter]`: Anger en tidsfördröjning i minuter innan avstängning eller omstart.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `shutdown`:

1. Stäng av systemet omedelbart:
    ```bash
    shutdown -h now
    ```

2. Starta om systemet omedelbart:
    ```bash
    shutdown -r now
    ```

3. Stäng av systemet efter 10 minuter:
    ```bash
    shutdown -h +10
    ```

4. Starta om systemet efter 5 minuter:
    ```bash
    shutdown -r +5
    ```

5. Skicka ett meddelande till användare innan avstängning:
    ```bash
    shutdown -h +1 "Systemet stängs av om 1 minut. Spara ditt arbete."
    ```

## Tips
- Använd `shutdown -c` för att avbryta en schemalagd avstängning.
- Informera alltid andra användare om en planerad avstängning för att undvika förlust av arbete.
- Kontrollera systemets loggar efter en avstängning eller omstart för att säkerställa att allt fungerade som det skulle.