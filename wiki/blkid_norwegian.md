# [Linux] Bash blkid bruk: Hente informasjon om blokk-enheter

## Oversikt
`blkid` er et Bash-kommando som brukes til å vise informasjon om blokk-enheter i Linux-systemer. Den gir detaljer om filsystemtype, UUID (Universally Unique Identifier) og andre metadata knyttet til lagringsenheter.

## Bruk
Den grunnleggende syntaksen for `blkid`-kommandoen er som følger:

```bash
blkid [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o, --output`: Angi formatet for utdataene (f.eks. `value`, `full`, `list`).
- `-s, --match-tag`: Filtrer utdataene basert på spesifikke tagger (f.eks. `UUID`, `TYPE`).
- `-p, --probe`: Utfør en probing av enhetene for å hente informasjon.
- `-c, --cache`: Bruk en cache-fil for å lagre informasjon om blokk-enheter.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `blkid`:

1. **Vis alle blokk-enheter**:
   ```bash
   blkid
   ```

2. **Vis spesifik informasjon om en bestemt enhet**:
   ```bash
   blkid /dev/sda1
   ```

3. **Filtrer utdata for kun UUID**:
   ```bash
   blkid -s UUID
   ```

4. **Bruke spesifikt utdataformat**:
   ```bash
   blkid -o value -s UUID /dev/sda1
   ```

5. **Bruke cache for raskere tilgang**:
   ```bash
   blkid -c /path/to/cachefile
   ```

## Tips
- Bruk `blkid` med `sudo` for å få tilgang til informasjon om alle enheter, spesielt hvis du får begrensede resultater.
- Lagre utdataene fra `blkid` til en fil for senere referanse ved å bruke omdirigering:
  ```bash
  blkid > blkid_output.txt
  ```
- Vær oppmerksom på at UUID-er er unike for hver enhet, så det er nyttig å bruke dem for å identifisere enheter i f.eks. fstab-filer.