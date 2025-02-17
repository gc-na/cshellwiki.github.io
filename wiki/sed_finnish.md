# [Linux] Bash sed käyttö: Tekstinkäsittely ja muokkaus

## Yleiskatsaus
`sed` (stream editor) on tehokas komentorivityökalu, jota käytetään tekstin muokkaamiseen ja käsittelyyn. Se mahdollistaa tekstin etsimisen, korvaamisen, poistamisen ja muokkaamisen reaaliaikaisesti.

## Käyttö
Perussyntaksi `sed`-komennolle on seuraava:

```bash
sed [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-e`: Mahdollistaa useiden komentojen suorittamisen.
- `-i`: Muokkaa tiedostoa paikan päällä (ilman tätä vaihtoehtoa tulostus tapahtuu vain konsoliin).
- `-n`: Estää tulostuksen, ellei sitä erikseen pyydetä.
- `s`: Korvaukselle käytettävä komento (esim. `s/vanha/uusi/`).

## Yleiset esimerkit

### 1. Tekstin korvaaminen
Korvataan kaikki esiintymät "vanha" sanalla "uusi" tiedostossa `esimerkki.txt`.

```bash
sed -i 's/vanha/uusi/g' esimerkki.txt
```

### 2. Rivin poistaminen
Poistetaan rivit, jotka sisältävät sanan "poista", tiedostosta `esimerkki.txt`.

```bash
sed -i '/poista/d' esimerkki.txt
```

### 3. Rivin numeron tulostaminen
Tulostetaan vain rivit 2-4 tiedostosta `esimerkki.txt`.

```bash
sed -n '2,4p' esimerkki.txt
```

### 4. Useiden komentojen suorittaminen
Suoritetaan useita komentoja yhdellä kertaa tiedostossa `esimerkki.txt`.

```bash
sed -e 's/vanha/uusi/g' -e 's/poista/korvata/g' esimerkki.txt
```

## Vinkit
- Käytä `-n`-vaihtoehtoa, kun haluat tarkastella vain tiettyjä tuloksia ilman ylimääräistä tulostusta.
- Testaa komento ensin ilman `-i`-vaihtoehtoa varmistaaksesi, että se toimii haluamallasi tavalla ennen tiedoston muokkaamista.
- Hyödynnä säännöllisiä lausekkeita monimutkaisemmissa hakuehdoissa ja korvauksissa.