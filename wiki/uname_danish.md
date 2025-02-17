# [Linux] Bash uname brug: Vis systeminformation

## Oversigt
`uname` er en Bash-kommando, der bruges til at vise systeminformation om den aktuelle maskine. Den kan give oplysninger om operativsystemet, kerneversionen og maskinens hardware.

## Brug
Den grundlæggende syntaks for `uname`-kommandoen er:

```bash
uname [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Viser alle tilgængelige systeminformationer.
- `-s`: Viser navnet på operativsystemet.
- `-n`: Viser netværksnavnet på maskinen.
- `-r`: Viser kerneversionen.
- `-v`: Viser versionsinformation om kerne.
- `-m`: Viser maskinens hardwarearkitektur.
- `-p`: Viser processorens type (hvis tilgængelig).
- `-i`: Viser hardwareplatformen (hvis tilgængelig).
- `-o`: Viser navnet på operativsystemet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `uname` kan bruges:

1. **Vis alle systeminformationer:**
   ```bash
   uname -a
   ```

2. **Vis operativsystemets navn:**
   ```bash
   uname -s
   ```

3. **Vis kerneversionen:**
   ```bash
   uname -r
   ```

4. **Vis maskinens hardwarearkitektur:**
   ```bash
   uname -m
   ```

5. **Vis netværksnavnet på maskinen:**
   ```bash
   uname -n
   ```

## Tips
- Brug `uname -a` for at få et hurtigt overblik over alle systemoplysninger på én gang.
- Kombiner `uname` med andre kommandoer som `grep` for at filtrere specifik information.
- Hvis du arbejder med scripts, kan `uname` hjælpe med at sikre, at din kode fungerer på forskellige systemer ved at tjekke operativsystemet og versionen.