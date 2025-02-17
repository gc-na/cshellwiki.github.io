# [Linux] Bash blkid käyttö: Tunnista laitteiden tiedostojärjestelmät

## Yleiskatsaus
`blkid`-komento on työkalu, jota käytetään tiedostojärjestelmien ja lohko-laitteiden tunnistamiseen Linux-järjestelmissä. Se näyttää laitteiden tiedot, kuten tiedostojärjestelmän tyypin ja UUID:n (Universally Unique Identifier).

## Käyttö
Perussyntaksi `blkid`-komennolle on seuraava:

```bash
blkid [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-o` tai `--output`: Määrittää tulostusmuodon (esim. `value`, `full`).
- `-s` tai `--subtype`: Määrittää, mitkä tiedot tulostetaan (esim. `UUID`, `TYPE`).
- `-p` tai `--probe`: Pakottaa komennon lukemaan laitteet, vaikka ne eivät olisi liitettyinä.
- `-c` tai `--cache`: Määrittää välimuistitiedoston käytön.

## Yleiset esimerkit
### 1. Näytä kaikki lohkolaiteet
```bash
blkid
```

### 2. Näytä vain tietyn laitteiston UUID
```bash
blkid /dev/sda1 -s UUID
```

### 3. Tulosta tiedostojärjestelmän tyyppi
```bash
blkid -o value -s TYPE /dev/sda1
```

### 4. Käytä välimuistia
```bash
blkid -c /path/to/cachefile
```

## Vinkit
- Käytä `blkid`-komentoa yhdessä `grep`-komennon kanssa, jos haluat suodattaa tuloksia tietyn tiedostojärjestelmän tyypin mukaan.
- Muista, että `blkid` vaatii usein root-oikeuksia, joten käytä `sudo`-komentoa tarvittaessa.
- Hyödynnä `-o`-vaihtoehtoa, jos haluat tulostaa vain tarvittavat tiedot, mikä tekee tuloksista helpommin luettavia.