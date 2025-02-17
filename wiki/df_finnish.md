# [Linux] Bash df käyttö: Tiedostojärjestelmän tilan tarkistaminen

## Yleiskatsaus
`df`-komento (disk free) on työkalu, jota käytetään tiedostojärjestelmien käytettävissä olevan tilan tarkistamiseen. Se näyttää, kuinka paljon levytilaa on käytettävissä ja kuinka paljon on käytetty eri tiedostojärjestelmissä.

## Käyttö
Perussyntaksi `df`-komennolle on seuraava:

```bash
df [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`: Näyttää tiedot ihmislukuisessa muodossa (esim. MB, GB).
- `-T`: Näyttää tiedostojärjestelmän tyypin.
- `-a`: Näyttää myös nollatilassa olevat tiedostojärjestelmät.
- `-i`: Näyttää inodejen käytön tiedostojärjestelmässä.

## Yleiset esimerkit

1. **Perustiedot kaikista tiedostojärjestelmistä**:
   ```bash
   df
   ```

2. **Ihmislukuisessa muodossa**:
   ```bash
   df -h
   ```

3. **Tiedostojärjestelmän tyypin näyttäminen**:
   ```bash
   df -T
   ```

4. **Kaikkien tiedostojärjestelmien näyttäminen, mukaan lukien tyhjät**:
   ```bash
   df -a
   ```

5. **Inodejen käytön tarkistaminen**:
   ```bash
   df -i
   ```

## Vinkit
- Käytä `-h`-vaihtoehtoa, jotta saat tulokset helpommin luettavassa muodossa.
- Tarkista säännöllisesti levytilan käyttö, erityisesti palvelimilla, jotta voit välttää tilan loppumisen.
- Yhdistä `df`-komento muihin komentoihin, kuten `grep`, suodattaaksesi tietoja tiettyjen tiedostojärjestelmien osalta. Esimerkiksi:
  ```bash
  df -h | grep /dev/sda1
  ```