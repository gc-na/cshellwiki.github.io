# [Linux] Bash ping6 brug: Tester netværksforbindelse med IPv6

## Overview
`ping6` er et værktøj, der bruges til at teste netværksforbindelsen til en IPv6-adresse. Det sender ICMP Echo Request-pakker til den angivne adresse og venter på svar, hvilket hjælper med at diagnosticere forbindelsesproblemer.

## Usage
Den grundlæggende syntaks for `ping6`-kommandoen er:

```bash
ping6 [options] [arguments]
```

## Common Options
- `-c <count>`: Angiver antallet af pakker, der skal sendes.
- `-i <interval>`: Sætter intervallet mellem pakkerne i sekunder.
- `-w <deadline>`: Angiver en tidsgrænse for, hvor længe der skal sendes pakker.
- `-s <size>`: Angiver størrelsen på de sendte pakker.

## Common Examples
Her er nogle praktiske eksempler på brugen af `ping6`:

1. **Ping en IPv6-adresse:**
   ```bash
   ping6 2001:db8::1
   ```

2. **Send 5 pakker til en IPv6-adresse:**
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. **Ændre intervallet mellem pakkerne til 2 sekunder:**
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. **Send pakker med en specifik størrelse:**
   ```bash
   ping6 -s 1280 2001:db8::1
   ```

5. **Sæt en tidsgrænse på 10 sekunder for at sende pakker:**
   ```bash
   ping6 -w 10 2001:db8::1
   ```

## Tips
- Brug `-c`-optionen for at begrænse antallet af pakker, så du ikke overbelaster netværket.
- Tjek din netværksforbindelse ved at pinge en kendt IPv6-adresse, som f.eks. en offentlig DNS-server.
- Vær opmærksom på firewall-indstillinger, der kan blokere ICMP-pakker, hvilket kan påvirke ping6-resultaterne.