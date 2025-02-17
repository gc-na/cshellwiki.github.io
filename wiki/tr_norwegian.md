# [Linux] Bash tr bruken: Konverterer eller fjerner tegn

## Oversikt
`tr` (translate) er en Bash-kommando som brukes til å konvertere eller fjerne tegn i tekst. Den er spesielt nyttig for å manipulere tekststrenger i kommandolinjen.

## Bruk
Den grunnleggende syntaksen for `tr`-kommandoen er som følger:

```bash
tr [alternativer] [argumenter]
```

## Vanlige alternativer
- `-d`: Fjerner de angitte tegnene fra input.
- `-s`: Komprimerer påfølgende forekomster av tegn til ett enkelt tegn.
- `-c`: Bruker komplementet av settet med tegn.

## Vanlige eksempler

### Eksempel 1: Erstatte små bokstaver med store bokstaver
For å konvertere små bokstaver til store bokstaver kan du bruke følgende kommando:

```bash
echo "hei verden" | tr 'a-z' 'A-Z'
```

### Eksempel 2: Fjerne spesifikke tegn
For å fjerne alle vokaler fra en tekst, kan du bruke:

```bash
echo "hei verden" | tr -d 'aeiou'
```

### Eksempel 3: Komprimere mellomrom
For å komprimere flere påfølgende mellomrom til ett enkelt mellomrom, kan du bruke:

```bash
echo "hei    verden" | tr -s ' '
```

### Eksempel 4: Erstatte tegn
For å erstatte komma med semikolon i en tekst, kan du bruke:

```bash
echo "hei, verden" | tr ',' ';'
```

## Tips
- Bruk `tr` i kombinasjon med andre kommandoer som `cat` eller `grep` for mer avansert tekstbehandling.
- Husk at `tr` ikke kan håndtere filer direkte; den må brukes med input fra stdin eller piped output.
- For mer komplekse tekstmanipuleringer, vurder å bruke `sed` eller `awk` i tillegg til `tr`.