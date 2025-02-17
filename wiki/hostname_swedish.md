# [Linux] Bash hostname användning: Hämta eller ställ in värdnamn

## Översikt
Kommandot `hostname` används för att visa eller ställa in systemets värdnamn. Värdnamnet är en identifierare för en dator i ett nätverk och kan vara användbart för nätverksadministration och identifiering av enheter.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
hostname [alternativ] [argument]
```

## Vanliga alternativ
- `-f`, `--fqdn`: Visar det fullständiga kvalificerade domännamnet (FQDN).
- `-i`, `--ip-address`: Visar IP-adressen för värdnamnet.
- `-s`, `--short`: Visar det korta värdnamnet utan domännamn.
- `-A`, `--all-fqdns`: Visar alla fullständiga kvalificerade domännamn för systemet.
- `--help`: Visar hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder kommandot `hostname`:

1. Visa det aktuella värdnamnet:
   ```bash
   hostname
   ```

2. Visa det fullständiga kvalificerade domännamnet:
   ```bash
   hostname -f
   ```

3. Visa IP-adressen för värdnamnet:
   ```bash
   hostname -i
   ```

4. Visa det korta värdnamnet:
   ```bash
   hostname -s
   ```

5. Ställ in ett nytt värdnamn (kräver root-åtkomst):
   ```bash
   sudo hostname ny-vardnamn
   ```

## Tips
- Kontrollera alltid vilket värdnamn som är inställt innan du gör ändringar, för att undvika förvirring i nätverksinställningarna.
- Använd `hostname -A` för att få en översikt över alla domännamn kopplade till systemet.
- Kom ihåg att ändringar av värdnamnet kan kräva en omstart av nätverksgränssnittet eller systemet för att träda i kraft.