# [Linux] Bash tput käyttö: Muotoile terminaalin ulkoasua

## Yleiskatsaus
`tput`-komento on työkalu, jota käytetään terminaalin ulkoasun muokkaamiseen. Sen avulla voit hallita tekstin värejä, muotoilua ja muita terminaalitoimintoja. Tämä tekee siitä hyödyllisen, kun haluat parantaa komentorivikäyttöliittymän visuaalista ilmettä.

## Käyttö
Perussyntaksi `tput`-komennolle on seuraava:

```bash
tput [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `setaf [n]`: Asettaa tekstin etuvärin (foreground color) numeroidun värin mukaan.
- `setab [n]`: Asettaa taustavärin (background color) numeroidun värin mukaan.
- `bold`: Asettaa tekstin lihavoiduksi.
- `smso`: Aktivoi korostustilan (standout mode).
- `rmso`: Poistaa korostustilan.

## Yleiset esimerkit
### 1. Tekstin värin asettaminen
Aseta teksti punaiseksi:

```bash
tput setaf 1
echo "Tämä teksti on punainen."
```

### 2. Taustavärin asettaminen
Aseta taustaväri vihreäksi:

```bash
tput setab 2
echo "Tämä teksti on vihreällä taustalla."
```

### 3. Lihavoitu teksti
Tulosta lihavoitu teksti:

```bash
tput bold
echo "Tämä teksti on lihavoitu."
tput sgr0  # Palauttaa oletusmuotoilun
```

### 4. Korostustilan käyttö
Tulosta teksti korostustilassa:

```bash
tput smso
echo "Tämä teksti on korostettu."
tput rmso  # Poistaa korostustilan
```

## Vinkit
- Käytä `tput sgr0`-komentoa palauttaaksesi kaikki muotoilut oletustilaan.
- Värien numerot voivat vaihdella terminaalista riippuen, joten kokeile eri numeroita nähdäksesi, mitkä värit toimivat parhaiten.
- Voit luoda skriptejä, jotka käyttävät `tput`-komentoa, jotta voit automatisoida terminaalin ulkoasun muokkaamisen.