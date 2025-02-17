# [Linux] Bash head användning: Visa de första raderna av en fil

## Översikt
Kommandot `head` används för att visa de första raderna av en fil. Det är särskilt användbart för att snabbt granska innehållet i stora filer utan att behöva öppna hela filen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
head [alternativ] [argument]
```

## Vanliga alternativ
- `-n [antal]`: Anger hur många rader som ska visas. Standardvärdet är 10.
- `-c [antal]`: Visar ett specifikt antal byte istället för rader.
- `-q`: Tyst läge, visar inte filnamn när flera filer anges.
- `-v`: Visar filnamn även i tyst läge.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `head`:

1. Visa de första 10 raderna av en fil:
   ```bash
   head fil.txt
   ```

2. Visa de första 5 raderna av en fil:
   ```bash
   head -n 5 fil.txt
   ```

3. Visa de första 20 byte av en fil:
   ```bash
   head -c 20 fil.txt
   ```

4. Visa de första 10 raderna av flera filer:
   ```bash
   head fil1.txt fil2.txt
   ```

5. Visa de första 10 raderna av en fil utan att visa filnamnet:
   ```bash
   head -q fil1.txt fil2.txt
   ```

## Tips
- Använd `head` tillsammans med andra kommandon genom att använda en pipe (`|`) för att filtrera resultat. Till exempel:
  ```bash
  ls -l | head -n 5
  ```
- Om du ofta behöver visa ett annat antal rader, kan du skapa en alias i din `.bashrc`-fil för att förenkla kommandot.
- Tänk på att `head` alltid visar de första raderna, så om du behöver se de sista raderna av en fil, överväg att använda kommandot `tail` istället.