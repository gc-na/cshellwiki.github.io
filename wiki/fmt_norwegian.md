# [Linux] Bash fmt Bruk: Formater tekstfiler

## Oversikt
`fmt` er et kommandolinjeverktøy i Unix-lignende operativsystemer som brukes til å formatere tekstfiler. Den justerer linjelengden i en tekst ved å bryte lange linjer og justere dem til et spesifisert antall tegn, noe som gjør teksten mer lesbar.

## Bruk
Den grunnleggende syntaksen for `fmt`-kommandoen er som følger:
```
fmt [alternativer] [argumenter]
```

## Vanlige alternativer
- `-w <antall>`: Angir maksimal linjelengde (standard er 75 tegn).
- `-s`: Slår av innrykk av linjer som allerede er innrykket.
- `-c`: Beholder innrykk av linjer og formaterer dem i henhold til det.

## Vanlige eksempler

### Eksempel 1: Formatere en tekstfil
For å formatere en tekstfil kalt `tekst.txt` til standard linjelengde:
```bash
fmt tekst.txt
```

### Eksempel 2: Angi maksimal linjelengde
For å formatere `tekst.txt` med en maksimal linjelengde på 50 tegn:
```bash
fmt -w 50 tekst.txt
```

### Eksempel 3: Beholde innrykk
For å formatere en fil samtidig som du beholder innrykk:
```bash
fmt -c tekst.txt
```

### Eksempel 4: Formatere flere filer
For å formatere flere filer på en gang:
```bash
fmt fil1.txt fil2.txt
```

## Tips
- Bruk `-w` alternativet for å tilpasse linjelengden til spesifikke krav i dokumentet ditt.
- Kombiner `fmt` med `cat` for å vise formaterte resultater direkte i terminalen:
  ```bash
  cat tekst.txt | fmt
  ```
- Vær oppmerksom på at `fmt` ikke endrer den originale filen, så hvis du ønsker å lagre endringene, kan du bruke omdirigering:
  ```bash
  fmt tekst.txt > formatert_tekst.txt
  ```