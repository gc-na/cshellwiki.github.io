# [Linux] Bash mkdir Bruk: Opprett kataloger

## Oversikt
`mkdir` (make directory) er en Bash-kommando som brukes til å opprette nye kataloger i filsystemet. Den er enkel å bruke og er et grunnleggende verktøy for organisering av filer og mapper.

## Bruk
Den grunnleggende syntaksen for `mkdir`-kommandoen er som følger:

```bash
mkdir [alternativer] [argumenter]
```

## Vanlige alternativer
- `-p`: Opprett foreldrekataloger hvis de ikke allerede eksisterer.
- `-v`: Vis en melding for hver katalog som opprettes.
- `-m`: Angi spesifikke tillatelser for den nye katalogen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `mkdir` kan brukes:

1. Opprett en enkel katalog:
   ```bash
   mkdir min_katalog
   ```

2. Opprett flere kataloger samtidig:
   ```bash
   mkdir katalog1 katalog2 katalog3
   ```

3. Opprett en katalog med foreldrekataloger:
   ```bash
   mkdir -p /sti/til/ny/katalog
   ```

4. Opprett en katalog og vis en melding:
   ```bash
   mkdir -v ny_katalog
   ```

5. Opprett en katalog med spesifikke tillatelser:
   ```bash
   mkdir -m 755 sikret_katalog
   ```

## Tips
- Bruk `-p` alternativet for å unngå feil når du oppretter flere nivåer av kataloger.
- Kombiner `mkdir` med andre kommandoer i skript for å automatisere opprettelsen av katalogstrukturer.
- Sjekk alltid at katalogen ikke allerede eksisterer for å unngå unødvendige feilmeldinger.