# [Linux] Bash dig användning: Hämta DNS-information

## Översikt
`dig` (Domain Information Groper) är ett kraftfullt verktyg för att hämta DNS-information. Det används för att fråga namnservrar och få detaljerad information om domännamn, inklusive IP-adresser och andra relaterade data.

## Användning
Den grundläggande syntaxen för `dig` är:

```bash
dig [alternativ] [argument]
```

## Vanliga alternativ
- `@server`: Ange en specifik DNS-server att fråga.
- `-t typ`: Ange typen av DNS-post att hämta (t.ex. A, MX, CNAME).
- `+short`: Visa en kortare version av svaret, vilket är användbart för att snabbt få IP-adresser.
- `+trace`: Följ hela DNS-upplösningsprocessen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `dig`:

1. Hämta A-posten för en domän:
   ```bash
   dig example.com
   ```

2. Hämta MX-posten för en domän:
   ```bash
   dig -t MX example.com
   ```

3. Använda en specifik DNS-server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Få en kort version av svaret:
   ```bash
   dig +short example.com
   ```

5. Spåra DNS-upplösningen:
   ```bash
   dig +trace example.com
   ```

## Tips
- Använd `+short` för att snabbt få IP-adresser utan all extra information.
- Testa olika DNS-servrar för att jämföra svarstider och resultat.
- Använd `dig` i skript för att automatisera DNS-frågor och övervakning.