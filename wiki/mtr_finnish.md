# [Linux] Bash mtr käyttö: Verkkoyhteyksien diagnosointi

## Yleiskatsaus
`mtr` (My Traceroute) on työkalu, joka yhdistää traceroute- ja ping-komennot. Se näyttää reitin, jota pakettitiedot seuraavat kohteeseen, sekä verkon viiveet ja pakettihäviöt. Tämä tekee siitä erinomaisen työkalun verkkoyhteyksien diagnosointiin ja ongelmien selvittämiseen.

## Käyttö
Perussyntaksi `mtr`-komennolle on seuraava:

```bash
mtr [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-r`: Tulostaa raportin, joka sisältää yhteenvedon reitistä.
- `-c [luku]`: Määrittää, kuinka monta pakettia lähetetään (esim. `-c 10`).
- `-i [aika]`: Asettaa aikavälin pakettien lähettämiselle (esim. `-i 1`).
- `-p`: Käynnistää mtr:n porttimonitorointitilan.
- `-w`: Näyttää tulokset "wide" -tilassa, joka on helpompi lukea.

## Yleiset esimerkit
1. **Perus mtr-käyttö**:
   ```bash
   mtr google.com
   ```
   Tämä komento näyttää reitin Googleen ja sen viiveet.

2. **Raportin luominen**:
   ```bash
   mtr -r google.com
   ```
   Tämä komento tuottaa yhteenvedon reitistä ilman jatkuvaa näyttöä.

3. **Pakettien määrän rajoittaminen**:
   ```bash
   mtr -c 5 google.com
   ```
   Tässä komennossa lähetetään vain 5 pakettia Googleen.

4. **Aikavälin asettaminen**:
   ```bash
   mtr -i 2 google.com
   ```
   Tämä komento lähettää paketteja 2 sekunnin välein.

## Vinkit
- Käytä `-r`-vaihtoehtoa, kun haluat saada nopean yhteenvedon reitistä ilman jatkuvaa näyttöä.
- Kokeile `-c`-vaihtoehtoa, jos haluat rajoittaa testin kestoa ja saada nopeita tuloksia.
- Muista tarkistaa verkon tilanne useammasta eri kohteesta, jotta saat kattavamman kuvan mahdollisista ongelmista.