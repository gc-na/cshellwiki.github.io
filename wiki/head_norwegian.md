# [Linux] Bash head bruk: Vis de første linjene i en fil

## Oversikt
`head`-kommandoen brukes til å vise de første linjene av en eller flere filer. Dette er nyttig når du ønsker å få et raskt innblikk i innholdet i en fil uten å åpne hele filen.

## Bruk
Grunnleggende syntaks for `head`-kommandoen er som følger:

```bash
head [alternativer] [argumenter]
```

## Vanlige alternativer
- `-n [antall]`: Angir hvor mange linjer som skal vises. Standard er 10 linjer.
- `-c [antall]`: Viser et spesifisert antall byte fra starten av filen.
- `-q`: Undertrykker filoverskrifter når flere filer vises.
- `-v`: Viser filoverskrifter selv når det bare vises én fil.

## Vanlige eksempler
Vis de første 10 linjene av en fil:

```bash
head filnavn.txt
```

Vis de første 5 linjene av en fil:

```bash
head -n 5 filnavn.txt
```

Vis de første 20 byte av en fil:

```bash
head -c 20 filnavn.txt
```

Vis de første 10 linjene fra flere filer:

```bash
head fil1.txt fil2.txt
```

## Tips
- Bruk `head` sammen med `tail` for å vise linjer fra midten av en fil. For eksempel, `tail -n +11 filnavn.txt | head -n 10` viser linjer 11 til 20.
- Kombiner `head` med `grep` for å filtrere linjer før du viser dem.
- Husk at `head` kan brukes med rørledninger for å vise utdata fra andre kommandoer. For eksempel, `ls -l | head` viser de første 10 linjene av en liste over filer.