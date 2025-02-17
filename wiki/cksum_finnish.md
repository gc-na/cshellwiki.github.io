# [Linux] Bash cksum käyttö: Tiedostojen tarkistussumman laskeminen

## Yleiskatsaus
`cksum`-komento laskee ja tulostaa tiedoston tarkistussumman (CRC) sekä tiedoston koon tavuina. Tämä komento on hyödyllinen tiedostojen eheystarkistuksessa ja varmistettaessa, että tiedostot eivät ole muuttuneet.

## Käyttö
Perussyntaksi `cksum`-komennolle on seuraava:
```bash
cksum [options] [arguments]
```

## Yleiset vaihtoehdot
- `-a, --algorithm ALGORITHM`: Määrittää käytettävän algoritmin tarkistussumman laskemiseen.
- `--help`: Näyttää ohjeet ja käytettävissä olevat vaihtoehdot.
- `--version`: Näyttää ohjelman version.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `cksum`-komennon käytöstä:

1. **Tarkistussumman laskeminen yhdelle tiedostolle:**
   ```bash
   cksum tiedosto.txt
   ```

2. **Tarkistussumman laskeminen useammalle tiedostolle kerralla:**
   ```bash
   cksum tiedosto1.txt tiedosto2.txt
   ```

3. **Tulostaa tarkistussumman ja koon tiedostosta, joka on syötetty putkessa:**
   ```bash
   cat tiedosto.txt | cksum
   ```

4. **Tarkistussumman laskeminen ja algoritmin määrittäminen:**
   ```bash
   cksum --algorithm crc32 tiedosto.txt
   ```

## Vinkit
- Käytä `cksum`-komentoa yhdessä `diff`-komennon kanssa varmistaaksesi, että tiedostot ovat identtisiä.
- Tallenna `cksum`-tulokset tiedostoon, jotta voit myöhemmin tarkistaa tiedostojen eheys.
- Muista, että `cksum`-komento ei ole yhtä turvallinen kuin muut salausalgoritmit, kuten `sha256sum`, mutta se on nopea ja helppokäyttöinen perus tarkistussumman laskemiseen.