# [Linux] Bash foreach bruk: Gjennomfør handlinger på hver element i en liste

## Oversikt
`foreach`-kommandoen brukes til å iterere over en liste av elementer og utføre en spesifikk handling for hvert element. Den er vanligvis brukt i skript for å automatisere oppgaver som krever repetisjon.

## Bruk
Den grunnleggende syntaksen for `foreach`-kommandoen er som følger:

```bash
foreach [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-n`: Kjør kommandoen uten å vise utdata.
- `-v`: Vis hvilke elementer som blir behandlet.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan `foreach` kan brukes:

### Eksempel 1: Enkle iterasjoner
```bash
foreach i (1 2 3 4 5)
    echo "Nummer: $i"
end
```
Dette skriptet vil skrive ut tallene fra 1 til 5.

### Eksempel 2: Filbehandling
```bash
foreach file (*.txt)
    mv $file /backup/
end
```
Her flyttes alle `.txt`-filer til en backup-mappe.

### Eksempel 3: Bruke variabler
```bash
set colors = (red green blue)
foreach color ($colors)
    echo "Fargen er: $color"
end
```
Dette skriptet vil skrive ut hver farge i listen.

## Tips
- Sørg for å bruke riktig syntaks for å unngå feil under kjøring.
- Test skriptene dine med et lite antall elementer før du kjører dem på større datasett.
- Bruk `-n` alternativet hvis du ønsker å kjøre skriptet uten å vise utdata, noe som kan være nyttig for lange prosesser.