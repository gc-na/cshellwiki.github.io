# [Linux] Bash hexdump Bruk: Vis hexadesimale representasjoner av filer

## Oversikt
Hexdump-kommandoen brukes til å vise innholdet i en fil i hexadesimal format. Dette er nyttig for å analysere binære filer, feilsøke data eller forstå hvordan data er lagret.

## Bruk
Den grunnleggende syntaksen for hexdump-kommandoen er som følger:

```bash
hexdump [alternativer] [argumenter]
```

## Vanlige alternativer
- `-C`: Vis hexdump med ASCII-representasjon ved siden av.
- `-n N`: Vis kun de første N byte av filen.
- `-s N`: Start dumping fra byteposisjon N.
- `-e FORMAT`: Angi et spesifikt format for utdataene.

## Vanlige eksempler

### Grunnleggende hexdump
For å vise innholdet i en fil i hexdump-format, kan du bruke:
```bash
hexdump filnavn.bin
```

### Hexdump med ASCII-representasjon
For å vise hexdump med ASCII-representasjon ved siden av, kan du bruke:
```bash
hexdump -C filnavn.bin
```

### Begrense antall byte
For å vise kun de første 16 byte av en fil, kan du bruke:
```bash
hexdump -n 16 filnavn.bin
```

### Starte dumping fra en spesifikk posisjon
For å starte dumping fra byteposisjon 10, kan du bruke:
```bash
hexdump -s 10 filnavn.bin
```

### Spesifikt format
For å bruke et spesifikt format for utdataene, kan du bruke:
```bash
hexdump -e '16/1 "%02x " "\n"' filnavn.bin
```

## Tips
- Bruk `-C` alternativet for å få en bedre forståelse av innholdet, spesielt når du jobber med tekstfiler.
- Kombiner `-n` og `-s` for å inspisere spesifikke deler av en fil.
- Lagre hexdump-utdataene til en fil ved å bruke omdirigering, for eksempel `hexdump filnavn.bin > utdata.txt`.