# [Linux] Bash zip bruk: Komprimere filer og mapper

## Oversikt
`zip` er et kommandolinjeverktøy som brukes til å komprimere filer og mapper til et enkelt arkivfilformat. Dette gjør det enklere å lagre og overføre flere filer som en enkelt enhet.

## Bruk
Den grunnleggende syntaksen for `zip`-kommandoen er som følger:

```bash
zip [alternativer] [arkivnavn.zip] [filer/mapper]
```

## Vanlige alternativer
- `-r`: Komprimerer mapper rekursivt.
- `-e`: Krypterer arkivet med et passord.
- `-9`: Bruker maksimal komprimering.
- `-d`: Sletter filer fra et eksisterende zip-arkiv.
- `-l`: Viser innholdet i et zip-arkiv.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `zip`-kommandoen:

### Komprimere en enkelt fil
For å komprimere en fil kalt `dokument.txt` til `dokument.zip`, kan du bruke følgende kommando:

```bash
zip dokument.zip dokument.txt
```

### Komprimere flere filer
For å komprimere flere filer, for eksempel `fil1.txt` og `fil2.txt`, kan du gjøre det slik:

```bash
zip arkiv.zip fil1.txt fil2.txt
```

### Komprimere en mappe rekursivt
For å komprimere en mappe kalt `prosjekt`, inkludert alle undermapper og filer, kan du bruke:

```bash
zip -r prosjekt.zip prosjekt/
```

### Kryptere et zip-arkiv
For å opprette et kryptert zip-arkiv, kan du bruke `-e`-alternativet:

```bash
zip -e sikret.zip fil1.txt fil2.txt
```

### Slette filer fra et zip-arkiv
For å slette en fil fra et eksisterende zip-arkiv, kan du bruke `-d`-alternativet:

```bash
zip -d arkiv.zip fil1.txt
```

## Tips
- Når du bruker `-r`, vær oppmerksom på at det kan ta lengre tid å komprimere store mapper.
- Husk å bruke `-9` for maksimal komprimering hvis filstørrelsen er viktig.
- Vær forsiktig med passordbeskyttelse; del aldri passordet via usikre kanaler.