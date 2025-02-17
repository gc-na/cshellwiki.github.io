# [Linux] Bash dirname käyttö: Hakee tiedostopolun hakemiston nimen

## Yleiskatsaus
`dirname`-komento on Bash-komento, joka palauttaa tiedostopolun hakemiston nimen. Se on hyödyllinen työkalu, kun haluat eristää tiedostopolun hakemiston osan tiedoston nimestä.

## Käyttö
Perussyntaksi `dirname`-komennolle on seuraava:

```bash
dirname [valinnat] [argumentit]
```

## Yleiset valinnat
- `-z`, `--zero`: Odottaa null-terminoituja syötteitä.
- `--help`: Näyttää apuviestin ja käytön.
- `--version`: Näyttää ohjelman version.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `dirname`-komennon käytöstä:

1. Hakee hakemiston nimen tiedostopolusta:
   ```bash
   dirname /home/kayttaja/tiedosto.txt
   ```
   Tämä palauttaa:
   ```
   /home/kayttaja
   ```

2. Hakee hakemiston nimen suhteellisesta polusta:
   ```bash
   dirname ./asiakirjat/raportti.pdf
   ```
   Tämä palauttaa:
   ```
   ./asiakirjat
   ```

3. Käyttämällä useita tiedostopolkuja yhdellä komennolla:
   ```bash
   dirname /var/log/syslog /usr/local/bin/script.sh
   ```
   Tämä palauttaa:
   ```
   /var/log
   /usr/local/bin
   ```

## Vinkit
- Voit yhdistää `dirname`-komennon muihin komentoihin, kuten `basename`, saadaksesi sekä hakemiston että tiedoston nimen yhdellä kertaa.
- Käytä `dirname`-komentoa skripteissä, kun sinun on käsiteltävä tiedostopolkuja ja haluat varmistaa, että käytät oikeita hakemistoja.
- Muista, että `dirname` palauttaa aina hakemiston nimen, joten tyhjät tiedostopolut voivat johtaa odottamattomiin tuloksiin.