# [Linux] Bash fsck bruk: Verifiser og reparer filsystemer

## Oversikt
`fsck` (file system check) er et verktøy i Linux som brukes til å kontrollere og reparere filsystemer. Det kan oppdage og rette opp feil i filsystemstrukturen, noe som er viktig for å opprettholde dataintegritet.

## Bruk
Grunnleggende syntaks for `fsck`-kommandoen er som følger:

```bash
fsck [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Automatisk reparasjon av feil uten å be om bekreftelse.
- `-n`: Kjør sjekken uten å gjøre noen endringer (kun lesemodus).
- `-y`: Svar ja på alle spørsmål om reparasjon.
- `-t`: Angi en spesifikk type filsystem for sjekk.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `fsck`:

1. Sjekk et spesifikt filsystem (for eksempel `/dev/sda1`):

   ```bash
   fsck /dev/sda1
   ```

2. Kjør `fsck` automatisk og reparer feil:

   ```bash
   fsck -a /dev/sda1
   ```

3. Sjekk et filsystem uten å gjøre endringer:

   ```bash
   fsck -n /dev/sda1
   ```

4. Svar ja på alle reparasjonsforespørselene:

   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Det er best å kjøre `fsck` på unmounted filsystemer for å unngå datatap.
- Planlegg regelmessige sjekker av filsystemet for å oppdage problemer tidlig.
- Vær forsiktig med `-y`-alternativet, da det kan føre til uventede endringer i filsystemet.