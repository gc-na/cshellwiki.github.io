# [Linux] Bash sha256sum käyttö: Lasketaan tiedostojen SHA-256-tarkistussummat

## Yleiskatsaus
`sha256sum` on Bash-komento, joka laskee ja tarkistaa tiedostojen SHA-256-tarkistussummat. Tämä komento on hyödyllinen tiedostojen eheys tarkistamisessa ja varmistamisessa, että tiedostot eivät ole vahingoittuneet tai muuttuneet.

## Käyttö
Perussyntaksi komennolle on seuraava:

```bash
sha256sum [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-b`, `--binary`: Käsittele tiedostoja binäärimuodossa.
- `-c`, `--check`: Tarkista tiedostojen tarkistussummat.
- `-t`, `--text`: Käsittele tiedostoja tekstimuodossa (oletusarvo).
- `--quiet`: Älä tulosta mitään, jos tarkistussumma on oikein.

## Yleiset esimerkit

### Tiedoston SHA-256-tarkistussumman laskeminen
Voit laskea tiedoston tarkistussumman seuraavalla komennolla:

```bash
sha256sum tiedosto.txt
```

### Useiden tiedostojen tarkistussumman laskeminen
Voit laskea useiden tiedostojen tarkistussummat yhdellä komennolla:

```bash
sha256sum tiedosto1.txt tiedosto2.txt
```

### Tarkistussumman tarkistaminen
Jos sinulla on tiedosto, jossa on tallennettu tarkistussummat, voit tarkistaa ne seuraavasti:

```bash
sha256sum -c tarkistussummat.txt
```

### Binäärimuotoisen tiedoston tarkistussumma
Jos haluat laskea binäärimuotoisen tiedoston tarkistussumman, käytä seuraavaa komentoa:

```bash
sha256sum -b binaritiedosto.bin
```

## Vinkit
- Varmista, että käytät `-c`-vaihtoehtoa tarkistaaksesi tiedostojen eheys, erityisesti latausten jälkeen.
- Tallenna tarkistussummat erilliseen tiedostoon, jotta voit tarkistaa ne myöhemmin.
- Käytä `--quiet`-vaihtoehtoa, jos haluat vain tietää, onko tarkistussumma oikein ilman ylimääräistä tulostetta.