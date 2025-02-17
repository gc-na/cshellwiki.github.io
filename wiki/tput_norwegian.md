# [Linux] Bash tput bruk: Kontrollere terminalens utseende

## Oversikt
`tput` er et Bash-kommando som brukes til å kontrollere terminalens utseende og oppførsel. Den gir mulighet for å sette farger, flytte markøren, og tilpasse tekstformatet i terminalvinduet.

## Bruk
Den grunnleggende syntaksen for `tput` er:

```bash
tput [alternativer] [argumenter]
```

## Vanlige alternativer
- `setaf`: Setter tekstfargen (foran).
- `setab`: Setter bakgrunnsfargen.
- `clear`: Tømmer terminalvinduet.
- `cup`: Flytter markøren til spesifisert rad og kolonne.
- `bold`: Setter teksten i fet skrift.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `tput`:

### Endre tekstfarge
For å endre tekstfargen til rød:

```bash
tput setaf 1
echo "Dette er rød tekst"
tput sgr0  # Tilbakestill til standard farge
```

### Endre bakgrunnsfarge
For å endre bakgrunnsfargen til blå:

```bash
tput setab 4
echo "Dette har blå bakgrunn"
tput sgr0  # Tilbakestill til standard bakgrunn
```

### Tømme terminalvinduet
For å tømme terminalvinduet:

```bash
tput clear
```

### Flytte markøren
For å flytte markøren til rad 5, kolonne 10:

```bash
tput cup 5 10
echo "Markøren er her"
```

### Fet tekst
For å skrive ut tekst i fet skrift:

```bash
tput bold
echo "Dette er fet tekst"
tput sgr0  # Tilbakestill til standard stil
```

## Tips
- Bruk `tput sgr0` for å tilbakestille terminalen til standardinnstillinger etter at du har gjort endringer.
- Du kan kombinere flere `tput`-kommandoer i en enkelt linje for å oppnå ønsket utseende.
- Sjekk terminalens fargepalett, da tilgjengelige farger kan variere mellom ulike terminaler.