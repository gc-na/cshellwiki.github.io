# [Linux] Bash cp Bruk: Kopier filer og kataloger

## Oversikt
`cp`-kommandoen brukes til å kopiere filer og kataloger i Unix-lignende operativsystemer. Den lar deg lage en kopi av en fil eller en hel katalogstruktur, noe som er nyttig for sikkerhetskopiering eller organisering av data.

## Bruk
Grunnleggende syntaks for `cp`-kommandoen er som følger:

```bash
cp [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-r`: Kopierer kataloger rekursivt.
- `-i`: Spør om bekreftelse før overskriving av eksisterende filer.
- `-u`: Kopierer bare filer som er nyere enn de eksisterende filene i mål.
- `-v`: Viser detaljer om hva som kopieres.
- `-a`: Bevarer filens attributter og kopierer rekursivt.

## Vanlige eksempler
Kopiere en enkelt fil:

```bash
cp fil.txt kopi_av_fil.txt
```

Kopiere en katalog rekursivt:

```bash
cp -r katalog/ kopi_av_katalog/
```

Kopiere en fil og spørre om bekreftelse før overskriving:

```bash
cp -i fil.txt kopi_av_fil.txt
```

Kopiere bare nyere filer:

```bash
cp -u fil.txt kopi_av_fil.txt
```

Kopiere en fil med detaljer om operasjonen:

```bash
cp -v fil.txt kopi_av_fil.txt
```

## Tips
- Bruk `-i`-alternativet for å unngå utilsiktet overskriving av filer.
- Når du kopierer kataloger, husk å alltid bruke `-r` for å sikre at innholdet i katalogen også blir kopiert.
- Kombiner alternativer for å tilpasse kommandoen etter behov, for eksempel `cp -avi` for å kopiere med detaljer og bekreftelse.