# [Linux] Bash ping brug: Tester netværksforbindelse

## Oversigt
`ping`-kommandoen bruges til at teste forbindelsen mellem din computer og en anden enhed på netværket. Den sender ICMP-echo-anmodninger til den angivne adresse og viser, hvor hurtigt svarene kommer tilbage, hvilket hjælper med at diagnosticere netværksproblemer.

## Brug
Den grundlæggende syntaks for `ping`-kommandoen er som følger:

```bash
ping [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c [antal]`: Angiver hvor mange pakker der skal sendes.
- `-i [sekunder]`: Angiver intervallet mellem pakkerne.
- `-s [størrelse]`: Angiver størrelsen på de data, der sendes.
- `-t [TTL]`: Angiver Time To Live for pakkerne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `ping` kan bruges:

1. **Ping en webadresse**:
   ```bash
   ping google.com
   ```

2. **Ping en IP-adresse med et begrænset antal pakker**:
   ```bash
   ping -c 4 192.168.1.1
   ```

3. **Ping med tilpasset pakke størrelse**:
   ```bash
   ping -s 100 8.8.8.8
   ```

4. **Ping med et specifikt interval mellem pakkerne**:
   ```bash
   ping -i 2 example.com
   ```

## Tips
- Brug `Ctrl + C` for at stoppe ping-kommandoen, hvis den kører kontinuerligt.
- Tjek netværksforbindelsen ved at ping en kendt adresse som `8.8.8.8` (Google DNS).
- Vær opmærksom på, at nogle servere kan blokere ping-anmodninger, hvilket kan give falske negative resultater.