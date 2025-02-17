# [Linux] Bash jobs käyttö: Näyttää taustatehtävät

## Overview
`jobs`-komento Bashissa näyttää käyttäjän käynnissä olevat taustatehtävät. Se on hyödyllinen työkalu, kun haluat hallita ja seurata prosesseja, jotka on käynnistetty taustalla.

## Usage
Perussyntaksi `jobs`-komennolle on seuraava:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Näyttää prosessin tunnukset (PID) jokaiselle taustatehtävälle.
- `-n`: Näyttää vain ne taustatehtävät, jotka ovat muuttuneet sen jälkeen, kun komento on viimeksi suoritettu.
- `-p`: Näyttää vain prosessitunnukset.

## Common Examples
1. **Peruskomento**: Näyttää kaikki taustatehtävät.
    ```bash
    jobs
    ```

2. **PID-tietojen näyttäminen**: Näyttää taustatehtävät prosessin tunnuksilla.
    ```bash
    jobs -l
    ```

3. **Uusien tehtävien tarkistaminen**: Näyttää vain ne taustatehtävät, jotka ovat muuttuneet.
    ```bash
    jobs -n
    ```

4. **Prosessitunnusten näyttäminen**: Näyttää vain prosessitunnukset.
    ```bash
    jobs -p
    ```

## Tips
- Käytä `bg`-komentoa siirtääksesi taustatehtävän taustalle, jos se on keskeytetty.
- Voit käyttää `fg`-komentoa tuodaksesi taustatehtävän eteen.
- Tarkista säännöllisesti taustatehtävät, erityisesti pitkään kestäviä prosesseja, varmistaaksesi, että ne toimivat odotetusti.