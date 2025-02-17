# [Linux] Bash vigr användning: Redigera systemets värdfil

## Översikt
Kommandot `vigr` används för att säkert redigera systemets värdfil (`/etc/hosts`). Det öppnar filen i en textredigerare och låser den för att förhindra att andra processer gör ändringar samtidigt. Detta är särskilt användbart för att undvika korruption av filen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
vigr [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Kontrollerar syntaxen på värdfilen innan den öppnas.
- `-h`: Visar hjälpmeddelande med tillgängliga alternativ.
- `-s`: Använder en specifik redigerare (t.ex. `nano` eller `vim`).

## Vanliga exempel
1. Öppna värdfilen med standardredigeraren:
   ```bash
   vigr
   ```

2. Kontrollera syntaxen på värdfilen innan redigering:
   ```bash
   vigr -c
   ```

3. Öppna värdfilen med `nano` som redigerare:
   ```bash
   vigr -s nano
   ```

## Tips
- Använd alltid `vigr` istället för att direkt redigera `/etc/hosts` med en vanlig textredigerare för att undvika potentiella problem med filkorruption.
- Kontrollera alltid syntaxen med `-c` alternativet innan du sparar ändringar för att säkerställa att inga fel finns.
- Bekanta dig med den redigerare du använder för att effektivt kunna navigera och göra ändringar i filen.