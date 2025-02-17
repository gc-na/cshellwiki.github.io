# [Linux] Bash mtr användning: Spåra nätverksvägar

## Översikt
Kommandot `mtr` (My Traceroute) kombinerar funktionerna av `ping` och `traceroute` för att ge en dynamisk och kontinuerlig visning av nätverksvägar. Det används för att diagnostisera nätverksproblem genom att visa hur data färdas genom nätverket och identifiera eventuella flaskhalsar.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
mtr [alternativ] [värd]
```

## Vanliga alternativ
- `-r`: Utför en rapportering och avsluta efter att ha samlat in data.
- `-c [antal]`: Ange hur många paket som ska skickas.
- `-i [sekunder]`: Ange intervallet mellan paket.
- `-p`: Visa portnummer i traceroute.
- `-n`: Använd IP-adresser istället för att lösa domännamn.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mtr`:

1. Spåra vägen till en värd:
   ```bash
   mtr example.com
   ```

2. Utföra en rapport och avsluta efter 10 paket:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Ange ett intervall på 2 sekunder mellan paketen:
   ```bash
   mtr -i 2 example.com
   ```

4. Visa IP-adresser istället för domännamn:
   ```bash
   mtr -n example.com
   ```

## Tips
- Använd `mtr` i kombination med `sudo` för att få mer detaljerad information om vissa nätverksvägar.
- För långvarig övervakning, överväg att köra `mtr` i bakgrunden och logga resultaten till en fil.
- Tänk på att vissa nätverksadministratörer kan blockera ICMP-paket, vilket kan påverka resultaten av `mtr`.