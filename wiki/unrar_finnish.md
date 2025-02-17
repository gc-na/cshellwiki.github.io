# [Linux] Bash unrar käyttö: Pakattujen tiedostojen purkaminen

## Yleiskatsaus
`unrar`-komento on työkalu, jota käytetään RAR-pakattujen tiedostojen purkamiseen. Se mahdollistaa RAR-arkistojen sisällön tarkastelun ja tiedostojen erottamisen arkistosta.

## Käyttö
Perussyntaksi `unrar`-komennolle on seuraava:

```bash
unrar [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `x`: Purkaa tiedostot nykyiseen hakemistoon.
- `e`: Purkaa tiedostot ilman hakemistorakennetta.
- `l`: Listaa arkiston sisällön.
- `t`: Testaa arkiston eheys.
- `v`: Näyttää yksityiskohtaisen tiedot purkamisesta.

## Yleiset esimerkit
1. **Tiedostojen purkaminen nykyiseen hakemistoon:**
   ```bash
   unrar x tiedosto.rar
   ```

2. **Tiedostojen purkaminen ilman hakemistorakennetta:**
   ```bash
   unrar e tiedosto.rar
   ```

3. **Arkiston sisällön listaaminen:**
   ```bash
   unrar l tiedosto.rar
   ```

4. **Arkiston eheyden testaaminen:**
   ```bash
   unrar t tiedosto.rar
   ```

5. **Purkaminen tiettyyn hakemistoon:**
   ```bash
   unrar x tiedosto.rar /polku/kohdehakemistoon/
   ```

## Vinkit
- Varmista, että sinulla on tarvittavat oikeudet purkaa tiedostoja kohdehakemistoon.
- Käytä `-y`-vaihtoehtoa, jos haluat ohittaa kysymykset tiedostojen ylikirjoittamisesta.
- Tarkista aina arkiston eheys ennen purkamista, erityisesti suurissa tai tärkeissä tiedostoissa.