# [Linux] Bash scp käyttö: Tiedostojen siirto turvallisesti

## Yleiskatsaus
`scp` (Secure Copy Protocol) on komentorivikäsky, jota käytetään tiedostojen siirtämiseen turvallisesti paikallisten ja etäpalvelimien välillä. Se hyödyntää SSH-protokollaa varmistaakseen, että tiedonsiirto on salattua ja turvallista.

## Käyttö
Perussyntaksi `scp`-komennolle on seuraava:

```bash
scp [vaihtoehdot] [lähde] [kohde]
```

## Yleiset vaihtoehdot
- `-r`: Siirtää hakemiston ja sen sisällön rekursiivisesti.
- `-P [portti]`: Määrittää SSH-portin, jota käytetään yhteyden muodostamiseen (huomaa, että iso P).
- `-i [avain]`: Käyttää määritettyä yksityistä avainta autentikointiin.
- `-v`: Näyttää yksityiskohtaisia tietoja siirron aikana, mikä on hyödyllistä virheiden vianetsinnässä.

## Yleiset esimerkit
### Tiedoston siirtäminen paikalliselta koneelta etäpalvelimelle
```bash
scp /polku/tiedostoon.txt käyttäjä@etäpalvelin:/polku/kohteeseen/
```

### Tiedoston siirtäminen etäpalvelimelta paikalliselle koneelle
```bash
scp käyttäjä@etäpalvelin:/polku/tiedostoon.txt /polku/kohteeseen/
```

### Hakemiston siirtäminen rekursiivisesti
```bash
scp -r /polku/hakemistoon käyttäjä@etäpalvelin:/polku/kohteeseen/
```

### Tiedoston siirtäminen eri portin kautta
```bash
scp -P 2222 /polku/tiedostoon.txt käyttäjä@etäpalvelin:/polku/kohteeseen/
```

## Vinkit
- Varmista, että sinulla on tarvittavat käyttöoikeudet sekä paikallisella että etäpalvelimella tiedostojen siirtämiseen.
- Käytä `-v`-vaihtoehtoa virheiden vianetsintään, jos tiedostonsiirto epäonnistuu.
- Harkitse SSH-avainten käyttöä salasanojen sijasta, jotta voit automatisoida siirtoja ilman käyttäjän syötettä.