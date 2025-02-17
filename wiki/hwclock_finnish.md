# [Linux] Bash hwclock käyttö: Ajan ja päivämäärän hallinta

## Yleiskatsaus
`hwclock`-komento on työkalu, jota käytetään järjestelmän kellon hallintaan. Se mahdollistaa sekä järjestelmän kellon että laitteiston kellon (RTC, Real-Time Clock) näyttämisen ja säätämisen. Tämä komento on erityisen hyödyllinen, kun halutaan varmistaa, että järjestelmän aika on synkronoitu oikein.

## Käyttö
Perussyntaksi `hwclock`-komennolle on seuraava:
```bash
hwclock [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `--show`: Näyttää nykyisen laitteiston kellon ajan.
- `--set`: Asettaa laitteiston kellon ajan.
- `--hctosys`: Asettaa järjestelmän kellon laitteiston kellon ajaksi.
- `--systohc`: Asettaa laitteiston kellon järjestelmän kellon ajaksi.
- `--utc`: Käyttää UTC-aikaa laitteiston kellossa.

## Yleiset esimerkit
1. **Näytä nykyinen laitteiston kellon aika:**
   ```bash
   hwclock --show
   ```

2. **Aseta laitteiston kello tiettyyn aikaan:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Aseta järjestelmän kello laitteiston kellon ajaksi:**
   ```bash
   hwclock --hctosys
   ```

4. **Aseta laitteiston kello järjestelmän kellon ajaksi:**
   ```bash
   hwclock --systohc
   ```

5. **Näytä laitteiston kello UTC-aikavyöhykkeessä:**
   ```bash
   hwclock --show --utc
   ```

## Vinkit
- Varmista, että sinulla on tarvittavat oikeudet käyttää `hwclock`-komentoa, sillä se saattaa vaatia järjestelmänvalvojan oikeuksia.
- Käytä `--utc`-vaihtoehtoa, jos käytät UTC-aikaa, jotta vältät aikavyöhykkeiden aiheuttamat ongelmat.
- Säännöllinen tarkistus ja synkronointi laitteiston kellon kanssa voi auttaa estämään aikavirheitä järjestelmässäsi.