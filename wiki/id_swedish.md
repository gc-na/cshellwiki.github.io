# [Linux] Bash id användning: visar användarens identitet

## Översikt
Kommandot `id` används för att visa användarens identitet och gruppinformation i ett Unix-liknande operativsystem. Det ger detaljer om användarens UID (User ID), GID (Group ID) och de grupper som användaren tillhör.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
id [alternativ] [argument]
```

## Vanliga alternativ
- `-u`: Visar endast användarens UID.
- `-g`: Visar endast användarens GID.
- `-G`: Visar alla grupper som användaren tillhör.
- `-n`: Används tillsammans med `-u` eller `-g` för att visa namnet istället för ID.
- `-r`: Visar det reella UID eller GID istället för det effektiva.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `id`-kommandot:

1. Visa användarens identitet:
   ```bash
   id
   ```

2. Visa endast användarens UID:
   ```bash
   id -u
   ```

3. Visa endast användarens GID:
   ```bash
   id -g
   ```

4. Visa alla grupper som användaren tillhör:
   ```bash
   id -G
   ```

5. Visa användarnamn istället för UID:
   ```bash
   id -un
   ```

## Tips
- Använd `id` för att snabbt kontrollera vilken användare och vilka grupper du är inloggad som, vilket kan vara användbart för felsökning.
- Kombinera `id` med andra kommandon för att skapa skript som automatiskt kontrollerar användarens rättigheter.
- Om du arbetar med flera användare, kan du ange ett användarnamn som argument för att få information om en specifik användare, till exempel:
  ```bash
  id användarnamn
  ```