# [Linux] Bash traceroute6 käyttö: Verkkoreittien jäljittäminen IPv6-osoitteille

## Yleiskatsaus
`traceroute6` on komento, jota käytetään IPv6-verkkojen reittien jäljittämiseen. Se näyttää, miten tiedot kulkevat verkon läpi ja mitkä reitittimet ovat mukana matkassa kohdeosoitteeseen.

## Käyttö
Perussyntaksi `traceroute6`-komennolle on seuraava:

```bash
traceroute6 [vaihtoehdot] [argumentit]
```

## Yhteiset vaihtoehdot
- `-m <max_hops>`: Määrittää maksimi hyppymäärän (reitittimien määrä), jonka jälkeen komento lopettaa.
- `-p <port>`: Määrittää portin, jota käytetään UDP-pakettien lähettämiseen.
- `-n`: Näyttää IP-osoitteet ilman DNS-nimiä.
- `-w <timeout>`: Asettaa aikarajan, jonka jälkeen pakettia ei odoteta.

## Yhteiset esimerkit
### Esimerkki 1: Perusreittijäljitys
Jäljitä reitti IPv6-osoitteeseen `2001:db8::1`:

```bash
traceroute6 2001:db8::1
```

### Esimerkki 2: Määritä maksimi hyppymäärä
Jäljitä reitti, mutta rajoita hyppyjen määrä viiteen:

```bash
traceroute6 -m 5 2001:db8::1
```

### Esimerkki 3: Näytä IP-osoitteet ilman DNS-nimiä
Jäljitä reitti ja näytä vain IP-osoitteet:

```bash
traceroute6 -n 2001:db8::1
```

### Esimerkki 4: Aikarajan asettaminen
Aseta aikaraja 2 sekuntia jokaiselle pakettivastaukselle:

```bash
traceroute6 -w 2 2001:db8::1
```

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos haluat nopeampia tuloksia ilman DNS-nimien selvittämistä.
- Tarkista, että IPv6 on käytössä järjestelmässäsi ennen `traceroute6`-komennon käyttöä.
- Hyödyntäminen yhdessä muiden verkon diagnostiikkatyökalujen, kuten `ping` ja `netstat`, kanssa voi antaa syvällisemmän käsityksen verkon toiminnasta.