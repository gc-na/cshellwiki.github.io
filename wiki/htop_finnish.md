# [Linux] Bash htop käyttö: Prosessien hallinta ja seuranta

## Yleiskatsaus
htop on interaktiivinen prosessinhallintatyökalu, joka tarjoaa käyttäjille mahdollisuuden seurata ja hallita järjestelmän prosesseja reaaliaikaisesti. Se tarjoaa visuaalisen käyttöliittymän, joka on helpompi käyttää kuin perinteinen `top`-komento.

## Käyttö
htop-komennon perussyntaksi on seuraava:

```bash
htop [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`, `--help`: Näyttää ohjeet ja käytön.
- `-s`, `--sort`: Määrittää, miten prosessit lajitellaan (esim. CPU, muisti).
- `-p`, `--pid`: Näyttää vain tietyt prosessit, jotka on määritetty PID:n mukaan.
- `-u`, `--user`: Näyttää vain tietyn käyttäjän prosessit.

## Yleiset esimerkit
- **Käynnistä htop**:
  ```bash
  htop
  ```

- **Lajittele prosessit muistin käytön mukaan**:
  ```bash
  htop -s MEM
  ```

- **Näytä vain tietyn käyttäjän prosessit**:
  ```bash
  htop -u käyttäjänimi
  ```

- **Näytä vain tietyt prosessit PID:n mukaan**:
  ```bash
  htop -p 1234,5678
  ```

## Vinkit
- Voit käyttää nuolinäppäimiä navigointiin ja `F9`-näppäimellä voit tappaa prosessin.
- Htopissa voit myös muuttaa prosessien prioriteettia (nice-arvoa) valitsemalla prosessin ja painamalla `F7` tai `F8`.
- Hyödynnä suodatusominaisuuksia (F3) etsiäksesi tiettyjä prosesseja nopeasti.