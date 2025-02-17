# [Linux] Bash killall Bruk: Avslutt prosesser etter navn

## Oversikt
`killall`-kommandoen brukes til å avslutte prosesser basert på prosessnavn. Dette er nyttig når du ønsker å stoppe alle forekomster av et bestemt program uten å måtte finne og avslutte hver enkelt prosess manuelt.

## Bruk
Grunnleggende syntaks for `killall`-kommandoen er som følger:

```bash
killall [alternativer] [argumenter]
```

## Vanlige alternativer
- `-u, --user <brukernavn>`: Avslutt prosesser som tilhører den spesifiserte brukeren.
- `-q, --quiet`: Ikke vis feilmeldinger for prosesser som ikke finnes.
- `-I, --ignore-case`: Ignorer store og små bokstaver i prosessnavnet.
- `-s, --signal <signal>`: Spesifiser hvilket signal som skal sendes til prosessene (standard er TERM).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `killall`:

1. Avslutt alle prosesser med navnet `firefox`:
   ```bash
   killall firefox
   ```

2. Avslutt alle prosesser med navnet `gedit`, og vis ikke feilmeldinger hvis prosessen ikke finnes:
   ```bash
   killall -q gedit
   ```

3. Avslutt alle prosesser som tilhører brukeren `john`:
   ```bash
   killall -u john
   ```

4. Send et spesifikt signal (f.eks. KILL) til alle prosesser med navnet `myapp`:
   ```bash
   killall -s KILL myapp
   ```

## Tips
- Vær forsiktig når du bruker `killall`, da det vil avslutte alle prosesser med det angitte navnet, noe som kan føre til tap av data hvis prosessene ikke er lagret.
- Bruk `-q`-alternativet for å unngå unødvendige feilmeldinger når du er usikker på om prosessen kjører.
- For å unngå utilsiktet avslutning av prosesser, kan det være lurt å bruke `pgrep` først for å se hvilke prosesser som vil bli påvirket.