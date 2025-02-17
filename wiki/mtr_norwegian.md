# [Linux] Bash mtr Bruk: Verktøy for nettverksdiagnose

## Oversikt
`mtr` (My Traceroute) er et kraftig verktøy som kombinerer funksjonaliteten til `ping` og `traceroute`. Det brukes til å diagnostisere nettverksproblemer ved å vise ruten datapakker tar til en vert, samt gi informasjon om tapte pakker og forsinkelse.

## Bruk
Grunnleggende syntaks for `mtr` er som følger:

```bash
mtr [alternativer] [vert]
```

## Vanlige alternativer
- `-r`: Kjør i rapportmodus og skriv ut resultatet til standard utgang.
- `-c <antall>`: Angi antall pakker som skal sendes.
- `-i <intervall>`: Angi intervall mellom sending av pakker i sekunder.
- `-p`: Kjør i "ping"-modus, bare send ping-pakker.
- `-n`: Bruk numeriske IP-adresser i stedet for å løse opp vertsnavn.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mtr`:

1. **Grunnleggende bruk mot en vert:**
   ```bash
   mtr example.com
   ```

2. **Kjøre i rapportmodus med 10 pakker:**
   ```bash
   mtr -r -c 10 example.com
   ```

3. **Angi intervall mellom pakker til 2 sekunder:**
   ```bash
   mtr -i 2 example.com
   ```

4. **Bruke numeriske IP-adresser:**
   ```bash
   mtr -n example.com
   ```

5. **Kjøre i ping-modus:**
   ```bash
   mtr -p example.com
   ```

## Tips
- Bruk `mtr` regelmessig for å overvåke nettverksytelse og identifisere problemer tidlig.
- Kombiner `mtr` med andre nettverksverktøy som `ping` og `traceroute` for mer omfattende feilsøking.
- Vær oppmerksom på at noen brannmurer kan blokkere `mtr`-forespørslene, så test alltid fra et passende nettverk.