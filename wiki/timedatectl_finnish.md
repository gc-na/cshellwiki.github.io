# [Linux] Bash timedatectl käyttö: Ajan ja päivämäärän hallinta

## Yleiskatsaus
`timedatectl` on komento, jota käytetään aikavyöhykkeiden, ajan ja päivämäärän hallintaan Linux-järjestelmissä. Sen avulla voit tarkistaa nykyiset aikasetukset, muuttaa aikavyöhykkeitä ja synkronoida järjestelmän kelloa.

## Käyttö
Perussyntaksi `timedatectl`-komennolle on seuraava:

```bash
timedatectl [options] [arguments]
```

## Yleiset vaihtoehdot
- `status`: Näyttää nykyiset aikasetukset ja aikavyöhykkeen.
- `set-time`: Asettaa järjestelmän kellon ajan.
- `set-timezone`: Muuttaa aikavyöhykettä.
- `set-ntp`: Ota käyttöön tai poista käytöstä NTP-synkronointi.
- `list-timezones`: Näyttää kaikki saatavilla olevat aikavyöhykkeet.

## Yleiset esimerkit

### Nykyisten aikasetusten tarkistaminen
Voit tarkistaa nykyiset aikasetukset ja aikavyöhykkeen käyttämällä seuraavaa komentoa:

```bash
timedatectl status
```

### Ajan asettaminen
Voit asettaa järjestelmän kellon ajan seuraavasti:

```bash
sudo timedatectl set-time '2023-10-01 12:00:00'
```

### Aikavyöhykkeen muuttaminen
Jos haluat muuttaa aikavyöhykettä, käytä seuraavaa komentoa:

```bash
sudo timedatectl set-timezone Europe/Helsinki
```

### NTP-synkronoinnin ottaminen käyttöön
Voit ottaa NTP-synkronoinnin käyttöön seuraavasti:

```bash
sudo timedatectl set-ntp true
```

### Aikavyöhykkeiden listaaminen
Kaikkien saatavilla olevien aikavyöhykkeiden listaamiseksi käytä komentoa:

```bash
timedatectl list-timezones
```

## Vinkit
- Varmista, että sinulla on tarvittavat oikeudet (esimerkiksi `sudo`) aikavyöhykkeen tai ajan muuttamiseen.
- Tarkista aikavyöhykkeet ennen muutoksia varmistaaksesi, että valitset oikean.
- Käytä `timedatectl`-komentoa säännöllisesti varmistaaksesi, että järjestelmän aika on synkronoitu oikein, erityisesti palvelimilla.