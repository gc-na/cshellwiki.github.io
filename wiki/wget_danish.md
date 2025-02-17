# [Linux] Bash wget brug: Hent filer fra internettet

## Oversigt
`wget` er et kraftfuldt kommandolinjeværktøj, der bruges til at hente filer fra internettet. Det understøtter forskellige protokoller som HTTP, HTTPS og FTP, hvilket gør det til et alsidigt valg for filoverførsler.

## Brug
Den grundlæggende syntaks for `wget` er som følger:

```bash
wget [muligheder] [argumenter]
```

## Almindelige muligheder
- `-O [filnavn]`: Gem den hentede fil med det angivne filnavn.
- `-c`: Fortsæt en afbrudt download.
- `-r`: Hent filer rekursivt.
- `-p`: Hent alle nødvendige filer for at vise en webside korrekt (f.eks. billeder og CSS).
- `--limit-rate=[hastighed]`: Begræns downloadhastigheden til den angivne værdi.

## Almindelige eksempler
Hent en fil fra en URL:

```bash
wget https://example.com/fil.zip
```

Hent en fil og gem den med et specifikt navn:

```bash
wget -O ny_fil.zip https://example.com/fil.zip
```

Fortsæt en afbrudt download:

```bash
wget -c https://example.com/fil.zip
```

Hent en hel webside rekursivt:

```bash
wget -r https://example.com
```

Hent en webside og alle dens nødvendige filer:

```bash
wget -p https://example.com
```

## Tips
- Brug `-q` for at køre wget i stille tilstand, så der ikke vises output i terminalen.
- Overvej at bruge `--limit-rate` for at undgå at overbelaste din internetforbindelse.
- Tjek altid URL'en for at sikre, at den er korrekt, før du starter en download.