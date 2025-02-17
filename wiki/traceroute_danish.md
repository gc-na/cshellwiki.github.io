# [Linux] Bash traceroute brug: Spore netværksruter

## Oversigt
Traceroute er et netværksdiagnoseværktøj, der bruges til at spore ruten, som datapakker tager fra en computer til en destination på internettet. Det viser hver hop (eller router) på vejen og den tid, det tager at nå hver hop, hvilket kan hjælpe med at identificere netværksproblemer.

## Brug
Den grundlæggende syntaks for traceroute-kommandoen er:

```bash
traceroute [muligheder] [argumenter]
```

## Almindelige muligheder
- `-m <hops>`: Angiver det maksimale antal hop, traceroute skal forsøge.
- `-w <sekunder>`: Angiver ventetiden for hver svarpakke.
- `-q <antal>`: Angiver antallet af forespørgsler, der sendes til hver hop.
- `-n`: Vis IP-adresser i stedet for at forsøge at opnå værtsnavne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger traceroute:

1. **Grundlæggende traceroute til en webadresse:**
   ```bash
   traceroute www.example.com
   ```

2. **Traceroute med maksimalt 10 hop:**
   ```bash
   traceroute -m 10 www.example.com
   ```

3. **Traceroute med ventetid på 2 sekunder:**
   ```bash
   traceroute -w 2 www.example.com
   ```

4. **Traceroute uden at opløse værtsnavne:**
   ```bash
   traceroute -n www.example.com
   ```

## Tips
- Brug `-n` muligheden for hurtigere resultater, hvis du ikke har brug for værtsnavne.
- Vær opmærksom på, at nogle routere kan være konfigureret til ikke at svare på traceroute-forespørgsler, hvilket kan resultere i "stille" hop.
- Hvis du oplever problemer med traceroute, kan det være nyttigt at køre kommandoen med `sudo` for at få flere oplysninger.