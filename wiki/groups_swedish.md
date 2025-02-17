# [Linux] Bash grupperar användare: Visa användargrupper

## Översikt
Kommandot `groups` används för att visa vilka grupper en specifik användare tillhör. Om inget användarnamn anges, visar det grupperna för den inloggade användaren. Detta är användbart för att snabbt få en översikt över användarens behörigheter och tillgångar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
groups [alternativ] [användarnamn]
```

## Vanliga alternativ
- `-h`, `--help`: Visar hjälpinformation för kommandot.
- `-V`, `--version`: Visar versionsinformation för kommandot.

## Vanliga exempel

1. Visa grupper för den inloggade användaren:
   ```bash
   groups
   ```

2. Visa grupper för en specifik användare, till exempel "alice":
   ```bash
   groups alice
   ```

3. Visa grupper för flera användare:
   ```bash
   groups alice bob
   ```

4. Visa hjälpinformation:
   ```bash
   groups --help
   ```

## Tips
- Använd `groups` för att snabbt kontrollera användarbehörigheter innan du tilldelar nya rättigheter.
- Om du är osäker på en användares grupper, kan du alltid använda kommandot utan argument för att kontrollera din egen status.
- Tänk på att vissa system kan ha begränsningar för att visa grupper för andra användare beroende på dina egna behörigheter.