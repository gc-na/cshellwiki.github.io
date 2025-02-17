# [Linux] Bash unxz käyttö: Pura .xz-tiedostoja

## Yleiskatsaus
`unxz` on komento, jota käytetään .xz-tiedostojen purkamiseen. Se on osa XZ-pakkaustyökalua ja mahdollistaa pakattujen tiedostojen palauttamisen alkuperäiseen muotoonsa.

## Käyttö
Perussyntaksi komennolle on seuraava:

```bash
unxz [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-k`, `--keep`: Säilyttää alkuperäisen .xz-tiedoston purkamisen jälkeen.
- `-f`, `--force`: Pakottaa purkamisen, vaikka tiedosto olisi jo olemassa tai se olisi vahingoittunut.
- `-v`, `--verbose`: Näyttää yksityiskohtaisempaa tietoa purkamisprosessista.

## Yleiset esimerkit
1. **Perustiedoston purkaminen**:
   ```bash
   unxz tiedosto.xz
   ```

2. **Alkuperäisen tiedoston säilyttäminen**:
   ```bash
   unxz -k tiedosto.xz
   ```

3. **Pakotettu purkaminen**:
   ```bash
   unxz -f tiedosto.xz
   ```

4. **Yksityiskohtainen purkaminen**:
   ```bash
   unxz -v tiedosto.xz
   ```

## Vinkit
- Käytä `-k`-vaihtoehtoa, jos haluat säilyttää alkuperäiset tiedostot varmuuden vuoksi.
- Tarkista aina tiedoston koko ja eheys ennen purkamista, erityisesti suurten tiedostojen kanssa.
- Voit yhdistää `unxz`-komennon putkistoon muiden komentojen kanssa, kuten `tar`, tiedostojen käsittelyn tehostamiseksi.