# [Linux] Bash lsmod användning: Visa laddade moduler

## Översikt
Kommandot `lsmod` används för att visa en lista över de kärnmoduler som för närvarande är laddade i Linux-kärnan. Det ger en översikt över vilka moduler som är aktiva och deras beroenden.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
lsmod [alternativ] [argument]
```

## Vanliga alternativ
- **-h, --help**: Visar hjälpmeddelande för kommandot.
- **-q, --quiet**: Visar endast nödvändig information, utan extra detaljer.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `lsmod`:

1. Visa alla laddade moduler:
   ```bash
   lsmod
   ```

2. Visa hjälpmeddelande:
   ```bash
   lsmod --help
   ```

3. Visa laddade moduler utan extra information:
   ```bash
   lsmod --quiet
   ```

## Tips
- Använd `lsmod` tillsammans med andra kommandon som `grep` för att filtrera resultatet. Till exempel, för att hitta en specifik modul:
  ```bash
  lsmod | grep modulnamn
  ```
- Det kan vara bra att köra `lsmod` som root-användare för att få mer detaljerad information om systemets moduler.