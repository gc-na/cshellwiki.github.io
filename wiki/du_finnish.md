# [Linux] Bash du käyttö: Tiedostojen ja kansioiden koon tarkistaminen

## Overview
`du` (disk usage) -komento on työkalu, jota käytetään tiedostojen ja kansioiden levytilan käytön tarkistamiseen. Se näyttää, kuinka paljon tilaa tiedostot ja kansiot vievät levyltä.

## Usage
Perussyntaksi `du`-komennolle on seuraava:

```bash
du [options] [arguments]
```

## Common Options
- `-h`: Näyttää koot ihmislukemassa muodossa (esim. Kt, Mt).
- `-s`: Näyttää vain yhteenvedon kunkin argumentin koosta.
- `-a`: Näyttää myös tiedostojen koot, ei vain kansioita.
- `-c`: Laskee yhteen kaikkien argumenttien koot ja näyttää summan.

## Common Examples
- Näytä kunkin kansion koko nykyisessä hakemistossa:
  ```bash
  du -h
  ```

- Näytä vain yhteenvedot kunkin kansion koosta:
  ```bash
  du -sh *
  ```

- Näytä kaikkien tiedostojen ja kansioiden koot ihmislukemassa muodossa:
  ```bash
  du -ah
  ```

- Laske yhteen kaikkien tiedostojen ja kansioiden koot ja näytä summa:
  ```bash
  du -ch *
  ```

## Tips
- Käytä `-h`-vaihtoehtoa, jotta saat koon helposti luettavassa muodossa.
- `-s`-vaihtoehto on hyödyllinen, kun haluat vain yhteenvedon ilman yksityiskohtia.
- Voit yhdistää useita vaihtoehtoja, kuten `du -sh`, saadaksesi haluamasi tiedot nopeasti.