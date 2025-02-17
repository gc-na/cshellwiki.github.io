# [Linux] Bash stat käyttö: Tiedostojen tilan tarkastaminen

## Yleiskatsaus
`stat`-komento on työkalu, jota käytetään tiedostojen ja hakemistojen tilan tarkastamiseen Linux-järjestelmässä. Se näyttää yksityiskohtaista tietoa tiedostosta, kuten sen koon, viimeisen muokkauksen ajan, käyttöoikeudet ja muita metatietoja.

## Käyttö
Perussyntaksi komennolle on seuraava:
```bash
stat [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c` : Määrittää mukautetun tulostusmuodon.
- `-f` : Näyttää tiedostojärjestelmän tilastot.
- `--format` : Määrittää tulostusmuodon tarkemmin.
- `-L` : Seuraa symbolisia linkkejä ja näyttää niiden kohdetiedoston tiedot.

## Yleiset esimerkit
Tässä on muutamia käytännön esimerkkejä `stat`-komennosta:

1. **Perustiedot tiedostosta**:
   ```bash
   stat tiedosto.txt
   ```

2. **Mukautettu tulostusmuoto**:
   ```bash
   stat -c '%n: %s bytes' tiedosto.txt
   ```

3. **Tiedostojärjestelmän tilastot**:
   ```bash
   stat -f /
   ```

4. **Symbolisen linkin seuraaminen**:
   ```bash
   stat -L linkki.txt
   ```

## Vinkit
- Käytä `-c`-vaihtoehtoa, jos haluat tulostaa vain tietyt tiedot tiedostosta.
- Voit yhdistää `stat`-komennon muihin komentoihin, kuten `grep`, suodataksesi tuloksia.
- Muista tarkistaa tiedoston käyttöoikeudet, erityisesti palvelimilla, joissa on useita käyttäjiä.