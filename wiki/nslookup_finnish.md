# [Linux] Bash nslookup käyttö: DNS-tietojen hakeminen

## Yleiskatsaus
`nslookup` on komento, jota käytetään DNS (Domain Name System) -tietojen hakemiseen. Sen avulla voit selvittää, mihin IP-osoitteeseen tietty verkkotunnus liittyy tai päinvastoin.

## Käyttö
Perussyntaksi `nslookup`-komennolle on seuraava:

```bash
nslookup [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-type=tyyppi`: Määrittää haettavan tietotyypin, kuten A, AAAA, MX, CNAME jne.
- `-timeout=n`: Asettaa aikarajan, kuinka kauan komento odottaa vastausta.
- `-retry=n`: Määrittää, kuinka monta kertaa komento yrittää uudelleen epäonnistuneen haun jälkeen.

## Yleiset esimerkit

### Verkkotunnuksen IP-osoitteen hakeminen
```bash
nslookup example.com
```

### IP-osoitteen kääntäminen verkkotunnukseksi
```bash
nslookup 93.184.216.34
```

### Tietotyypin määrittäminen (esimerkiksi MX-tietueet)
```bash
nslookup -type=MX example.com
```

### Aikarajan asettaminen
```bash
nslookup -timeout=5 example.com
```

## Vinkit
- Käytä `-type`-vaihtoehtoa, jos tarvitset erityisiä tietoja, kuten sähköpostipalvelimien osoitteita.
- Muista, että `nslookup` voi olla hyödyllinen myös vianetsinnässä, kun yrität selvittää verkkoyhteysongelmia.
- Testaa eri DNS-palvelimia lisäämällä niiden osoitteet komennon loppuun, esimerkiksi `nslookup example.com 8.8.8.8` (Google DNS).