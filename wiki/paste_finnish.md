# [Linux] Bash paste käyttö: Yhdistää tiedostoja riveittäin

## Yleiskatsaus
`paste`-komento on Bash-komento, jota käytetään yhdistämään tiedostoja riveittäin. Se ottaa useita tiedostoja syötteenä ja yhdistää niiden rivit yhdeksi riviksi, erottamalla ne oletusarvoisesti tabulaattorilla.

## Käyttö
Perussyntaksi `paste`-komennolle on seuraava:

```bash
paste [options] [arguments]
```

## Yleiset vaihtoehdot
- `-d`: Määrittelee erottimen, jota käytetään rivien välillä. Oletusarvo on tabulaattori.
- `-s`: Yhdistää tiedoston rivit sarakkeittain sen sijaan, että se yhdistäisi eri tiedostojen rivejä.
- `-z`: Käyttää nollan merkkijonoa rivierottimena.

## Yleiset esimerkit
Yhdistetään kaksi tiedostoa rivittäin:

```bash
paste file1.txt file2.txt
```

Määritellään erottimeksi pilkku:

```bash
paste -d ',' file1.txt file2.txt
```

Yhdistetään tiedoston rivit sarakkeittain:

```bash
paste -s file1.txt
```

Käytetään nollan merkkijonoa rivierottimena:

```bash
paste -z file1.txt file2.txt
```

## Vinkit
- Käytä `-d`-vaihtoehtoa, jos haluat käyttää erottimena muuta kuin tabulaattoria, kuten pilkkua tai puolipistettä.
- Muista, että `paste` yhdistää tiedostot riveittäin, joten varmista, että tiedostot ovat oikeassa järjestyksessä.
- Voit yhdistää useita tiedostoja kerralla, mikä tekee `paste`-komennosta tehokkaan työkalun datan yhdistämiseen.