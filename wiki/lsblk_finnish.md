# [Linux] Bash lsblk käyttö: Näyttää lohkotiedostojärjestelmät

## Yleiskatsaus
`lsblk` on komento, jota käytetään näyttämään lohkotiedostojärjestelmät ja niiden tiedot Linux-järjestelmässä. Se listaa kaikki lohkot, kuten kiintolevyt, SSD:t ja niiden osiot, sekä näyttää niiden koko- ja liitostiedot.

## Käyttö
Perussyntaksi `lsblk`-komennolle on seuraava:

```bash
lsblk [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-a`, `--all`: Näyttää myös tyhjät lohkot.
- `-f`, `--fs`: Näyttää tiedostojärjestelmän tiedot.
- `-l`, `--list`: Näyttää tiedot listamuodossa.
- `-o`, `--output`: Määrittelee näytettävät sarakkeet.
- `-n`, `--noheadings`: Poistaa otsikkorivin tulosteesta.

## Yleiset esimerkit

1. **Peruskomento**: Näyttää kaikki lohkotiedostojärjestelmät.
   ```bash
   lsblk
   ```

2. **Näytä tiedostojärjestelmän tiedot**: Lisää tiedostojärjestelmän tiedot tulosteeseen.
   ```bash
   lsblk -f
   ```

3. **Listamuoto**: Näyttää lohkot listamuodossa.
   ```bash
   lsblk -l
   ```

4. **Mukautettu tuloste**: Näyttää vain tietyt sarakkeet, kuten laitteen nimen ja koon.
   ```bash
   lsblk -o NAME,SIZE
   ```

5. **Näytä myös tyhjät lohkot**: Näyttää kaikki lohkot, mukaan lukien tyhjät.
   ```bash
   lsblk -a
   ```

## Vinkit
- Käytä `lsblk -f` -komentoa saadaksesi kattavampaa tietoa tiedostojärjestelmistä, kuten tyyppi ja UUID.
- Hyödynnä `-o`-vaihtoehtoa mukauttaaksesi tulosteen juuri sellaiseksi kuin tarvitset.
- Muista, että `lsblk` ei vaadi pääkäyttäjäoikeuksia, joten voit käyttää sitä tavallisena käyttäjänä.