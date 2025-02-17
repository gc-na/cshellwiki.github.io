# [Linux] Bash service käyttö: Palveluiden hallinta

## Overview
`service`-komento on työkalu, jota käytetään järjestelmäpalveluiden hallintaan Linux-järjestelmissä. Sen avulla voit käynnistää, pysäyttää, uudelleenkäynnistää ja tarkistaa palveluiden tilan.

## Usage
Perussyntaksi `service`-komennolle on seuraava:

```bash
service [palvelu] [toiminto]
```

## Common Options
- `start`: Käynnistää määritellyn palvelun.
- `stop`: Pysäyttää määritellyn palvelun.
- `restart`: Uudelleenkäynnistää määritellyn palvelun.
- `status`: Näyttää määritellyn palvelun nykyisen tilan.

## Common Examples
- Palvelun käynnistäminen:
  ```bash
  service apache2 start
  ```
  
- Palvelun pysäyttäminen:
  ```bash
  service mysql stop
  ```

- Palvelun uudelleenkäynnistäminen:
  ```bash
  service nginx restart
  ```

- Palvelun tilan tarkistaminen:
  ```bash
  service ssh status
  ```

## Tips
- Varmista, että sinulla on tarvittavat oikeudet palveluiden hallintaan, yleensä tämä vaatii pääkäyttäjän oikeudet.
- Käytä `status`-komentoa ennen palvelun käynnistämistä tai pysäyttämistä, jotta tiedät palvelun nykyisen tilan.
- Muista, että jotkin palvelut saattavat käyttää `systemctl`-komentoa, joten tarkista järjestelmäsi dokumentaatio, jos `service` ei toimi odotetusti.