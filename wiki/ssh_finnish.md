# [Linux] Bash ssh käyttö: Etäyhteyksien luominen

## Yleiskatsaus
`ssh` (Secure Shell) on protokolla, joka mahdollistaa turvallisen etäyhteyden muodostamisen toiseen tietokoneeseen. Se tarjoaa salatun yhteyden, jonka avulla käyttäjät voivat hallita etäkoneita ja siirtää tietoja turvallisesti.

## Käyttö
Perussyntaksi `ssh`-komennolle on seuraava:

```bash
ssh [vaihtoehdot] [käyttäjä@isäntä]
```

## Yleiset vaihtoehdot
- `-p [portti]`: Määrittää käytettävän portin (oletus on 22).
- `-i [avain]`: Käyttää määritettyä yksityistä avainta autentikointiin.
- `-v`: Näyttää yksityiskohtaisia tietoja yhteyden muodostamisesta (debugging).
- `-X`: Mahdollistaa X11-ikkunoiden siirron etäyhteyden kautta.

## Yleiset esimerkit
### Yhteyden muodostaminen etäkoneeseen
```bash
ssh käyttäjä@esimerkki.com
```

### Yhteyden muodostaminen tiettyyn porttiin
```bash
ssh -p 2222 käyttäjä@esimerkki.com
```

### Yksityisen avaimen käyttäminen
```bash
ssh -i ~/.ssh/id_rsa käyttäjä@esimerkki.com
```

### X11-ikkunoiden siirto
```bash
ssh -X käyttäjä@esimerkki.com
```

## Vinkit
- Käytä avainpohjaista autentikointia salasanojen sijaan turvallisuuden parantamiseksi.
- Määritä `~/.ssh/config`-tiedostoon usein käytetyt isännät, jotta voit lyhentää komentoja.
- Hyödynnä `-v`-vaihtoehtoa ongelmien vianetsintään, jos yhteyden muodostaminen epäonnistuu.