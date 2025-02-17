# [Linux] Bash rm Bruk: Fjerne filer og kataloger

## Oversikt
`rm`-kommandoen brukes til å fjerne filer og kataloger i Unix-lignende operativsystemer. Det er en kraftig kommando som permanent sletter spesifiserte filer, så det er viktig å bruke den med forsiktighet.

## Bruk
Grunnleggende syntaks for `rm`-kommandoen er som følger:

```bash
rm [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Tvinger sletting uten å spørre om bekreftelse.
- `-i`: Ber om bekreftelse før hver fil slettes.
- `-r`: Fjerner kataloger og deres innhold rekursivt.
- `-v`: Viser detaljer om hva som blir slettet.

## Vanlige eksempler
Slette en enkelt fil:

```bash
rm filnavn.txt
```

Slette flere filer samtidig:

```bash
rm fil1.txt fil2.txt fil3.txt
```

Slette en katalog og alt innholdet i den:

```bash
rm -r katalognavn
```

Tvinge sletting uten bekreftelse:

```bash
rm -f filnavn.txt
```

Slette filer med bekreftelse:

```bash
rm -i filnavn.txt
```

## Tips
- Bruk `-i` alternativet for å unngå utilsiktet sletting av viktige filer.
- Vær forsiktig med `-r` alternativet, spesielt når du sletter kataloger, da dette kan føre til tap av mange filer.
- Vurder å bruke `trash-cli` eller lignende verktøy for å kunne gjenopprette filer etter sletting.