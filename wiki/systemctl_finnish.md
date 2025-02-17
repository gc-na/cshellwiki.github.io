# [Linux] Bash systemctl käyttö: Palveluiden hallinta

## Yleiskatsaus
`systemctl` on komento, jota käytetään Linux-järjestelmissä palveluiden ja järjestelmän tilan hallintaan. Se on osa systemd-järjestelmää, joka on moderni alusta palveluiden ja prosessien hallintaan.

## Käyttö
Perussyntaksi `systemctl`-komennolle on seuraava:
```bash
systemctl [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `start`: Käynnistää palvelun.
- `stop`: Pysäyttää palvelun.
- `restart`: Käynnistää palvelun uudelleen.
- `status`: Näyttää palvelun nykyisen tilan.
- `enable`: Ota palvelu käyttöön käynnistyksessä.
- `disable`: Poista palvelu käytöstä käynnistyksessä.

## Yleiset esimerkit
### Palvelun käynnistäminen
```bash
sudo systemctl start nginx
```

### Palvelun pysäyttäminen
```bash
sudo systemctl stop nginx
```

### Palvelun tilan tarkistaminen
```bash
systemctl status nginx
```

### Palvelun ottaminen käyttöön käynnistyksessä
```bash
sudo systemctl enable nginx
```

### Palvelun poistaminen käytöstä käynnistyksessä
```bash
sudo systemctl disable nginx
```

## Vinkit
- Käytä `sudo`-komentoa, jos tarvitset pääkäyttäjän oikeuksia palveluiden hallintaan.
- Tarkista palvelun lokitiedostot ongelmien selvittämiseksi komennolla `journalctl -u [palvelu]`.
- Hyödynnä `systemctl list-units` nähdäksesi kaikki aktiiviset palvelut ja niiden tilat.