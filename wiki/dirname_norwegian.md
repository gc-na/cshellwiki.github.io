# [Linux] Bash dirname Bruk: Hent katalognavn fra en filbane

## Oversikt
`dirname`-kommandoen brukes til å hente katalognavnet fra en spesifisert filbane. Den returnerer den delen av stien som representerer katalogen, og fjerner filnavnet.

## Bruk
Grunnleggende syntaks for `dirname`-kommandoen er:

```bash
dirname [alternativer] [argumenter]
```

## Vanlige alternativer
- `-z`: Behandler null-terminerte strenger.
- `--help`: Viser hjelp og informasjon om bruken av kommandoen.
- `--version`: Viser versjonsinformasjon om `dirname`.

## Vanlige eksempler

### Eksempel 1: Hente katalognavn
For å hente katalognavnet fra en filbane:

```bash
dirname /home/user/documents/file.txt
```
**Utdata:** `/home/user/documents`

### Eksempel 2: Hente katalognavn fra relativ bane
Når du bruker en relativ bane:

```bash
dirname documents/file.txt
```
**Utdata:** `documents`

### Eksempel 3: Hente katalognavn fra flere filer
Du kan også bruke `dirname` med flere filer:

```bash
dirname /home/user/documents/file1.txt /home/user/documents/file2.txt
```
**Utdata:**
```
/home/user/documents
/home/user/documents
```

## Tips
- Bruk `dirname` sammen med `basename` for å dele opp filbaner i katalog- og filnavn.
- Vær oppmerksom på at `dirname` alltid returnerer en sti, selv om den er tom hvis filbanen er en rotbane.
- Når du jobber med skript, kan det være nyttig å lagre katalognavnet i en variabel for senere bruk.