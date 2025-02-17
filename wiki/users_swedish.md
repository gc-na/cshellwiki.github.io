# [Linux] Bash-användare användning: Visa användarinformation

## Översikt
Kommandot `users` används för att visa namnen på de användare som för närvarande är inloggade på systemet. Det ger en snabb översikt över aktiva användarsessioner.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
users [alternativ]
```

## Vanliga alternativ
- `-n`: Visar endast antalet inloggade användare.
- `-r`: Visar endast användare som är inloggade på en terminal som är aktiv.

## Vanliga exempel
Här är några praktiska exempel på hur man använder kommandot `users`:

1. Visa alla inloggade användare:
   ```bash
   users
   ```

2. Visa antalet inloggade användare:
   ```bash
   users -n
   ```

3. Visa användare på aktiva terminaler:
   ```bash
   users -r
   ```

## Tips
- Använd `who`-kommandot för att få mer detaljerad information om inloggade användare, inklusive deras inloggningstid och terminal.
- Kombinera `users` med andra kommandon som `wc -w` för att räkna antalet inloggade användare:
  ```bash
  users | wc -w
  ```