# [Linux] Bash who användning: Visa inloggade användare

## Översikt
Kommandot `who` används för att visa en lista över användare som för närvarande är inloggade på systemet. Det visar information som användarnamn, terminal, inloggningstid och mer.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
who [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar all tillgänglig information, inklusive inloggningstider och terminalstatus.
- `-b`: Visar när systemet senast startades.
- `-q`: Visar en sammanfattning av inloggade användare och antalet inloggade användare.
- `--help`: Visar hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `who`:

1. Visa en lista över alla inloggade användare:
   ```bash
   who
   ```

2. Visa all tillgänglig information om inloggade användare:
   ```bash
   who -a
   ```

3. Visa när systemet senast startades:
   ```bash
   who -b
   ```

4. Visa en sammanfattning av inloggade användare:
   ```bash
   who -q
   ```

## Tips
- Använd `who` tillsammans med andra kommandon som `grep` för att filtrera resultaten. Till exempel, för att hitta en specifik användare:
  ```bash
  who | grep användarnamn
  ```
- För att få mer detaljerad information om användare, överväg att använda kommandot `w`, som också visar vad användarna gör.
- Kom ihåg att `who` kan kräva administratörsrättigheter för att visa vissa användardata beroende på systemets säkerhetsinställningar.