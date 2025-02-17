# [Linux] Bash traceroute6 brug: Spor IPv6-netværksruter

## Oversigt
`traceroute6` er et værktøj, der bruges til at spore ruten, som IPv6-pakker tager gennem et netværk. Det viser hver hop (router) på vejen til destinationen, hvilket kan være nyttigt til fejlfinding af netværksproblemer.

## Brug
Den grundlæggende syntaks for `traceroute6`-kommandoen er:

```bash
traceroute6 [muligheder] [argumenter]
```

## Almindelige muligheder
- `-m <max_hops>`: Angiver det maksimale antal hop, der skal spores.
- `-p <port>`: Angiver portnummeret, der skal bruges til at sende pakker.
- `-w <timeout>`: Angiver timeout-værdien for hver anmodning i sekunder.
- `-n`: Undgår at oversætte IP-adresser til værtsnavne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `traceroute6`:

1. Spore ruten til en IPv6-adresse:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spore ruten med et maksimalt antal hop på 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

3. Spore ruten til en IPv6-adresse og undgå navneopslag:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

4. Spore ruten og angive en specifik port:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

## Tips
- Brug `-n` muligheden for hurtigere resultater, da det undgår DNS-opslag.
- Vær opmærksom på, at nogle netværk kan blokere traceroute-pakker, hvilket kan resultere i ufuldstændige eller ingen resultater.
- Tjek altid, at du har de nødvendige tilladelser til at køre traceroute6, især på offentlige netværk.