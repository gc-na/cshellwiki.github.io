# [Linux] Bash host brug: Hent DNS-oplysninger

## Oversigt
`host` er et kommandolinjeværktøj, der bruges til at udføre DNS-opslag. Det kan konvertere domænenavne til IP-adresser og omvendt, hvilket gør det nyttigt til fejlfinding af netværksproblemer og til at få oplysninger om domæner.

## Brug
Den grundlæggende syntaks for `host`-kommandoen er:

```bash
host [options] [arguments]
```

## Almindelige muligheder
- `-a`: Vis alle oplysninger om domænet.
- `-t <type>`: Angiv typen af DNS-opslag, f.eks. A, MX, TXT.
- `-v`: Aktivér detaljeret udskrift.
- `-l`: Udfør en zoneoverførsel (kun for autoritative servere).

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `host`-kommandoen kan bruges:

1. **Find IP-adressen for et domæne:**
   ```bash
   host example.com
   ```

2. **Find domænenavnet for en IP-adresse:**
   ```bash
   host 93.184.216.34
   ```

3. **Få MX-poster for et domæne:**
   ```bash
   host -t MX example.com
   ```

4. **Vis alle oplysninger om et domæne:**
   ```bash
   host -a example.com
   ```

5. **Udfør en zoneoverførsel:**
   ```bash
   host -l example.com ns1.example.com
   ```

## Tips
- Brug `-v` for at få mere detaljerede oplysninger, når du fejlfinder DNS-problemer.
- Kombiner `host` med andre kommandolinjeværktøjer som `grep` for at filtrere output.
- Vær opmærksom på, at zoneoverførsler kun fungerer, hvis du har tilladelse til at tilgå den autoritative DNS-server.