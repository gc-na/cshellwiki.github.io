# [Linux] Bash ftp käyttö: Tiedostojen siirtäminen verkossa

## Yleiskatsaus
`ftp` (File Transfer Protocol) on komentorivipohjainen työkalu, jota käytetään tiedostojen siirtämiseen verkon yli. Se mahdollistaa tiedostojen lataamisen ja lähettämisen palvelimille ja asiakkaille.

## Käyttö
Perussyntaksi `ftp`-komennolle on seuraava:

```bash
ftp [options] [arguments]
```

## Yleiset vaihtoehdot
- `-i`: Poistaa interaktiivisen tilan, jolloin tiedostot siirretään ilman vahvistusta.
- `-v`: Näyttää yksityiskohtaisemman tulosteen siirroista.
- `-n`: Estää automaattisen kirjautumisen, jolloin käyttäjän on syötettävä kirjautumistiedot manuaalisesti.

## Yleiset esimerkit
### Yhdistäminen FTP-palvelimeen
```bash
ftp ftp.example.com
```

### Kirjautuminen käyttäjätunnuksella
```bash
ftp -n ftp.example.com
```
Syötä sitten käyttäjätunnus ja salasana manuaalisesti.

### Tiedoston lataaminen palvelimelta
```bash
get tiedosto.txt
```

### Tiedoston lähettäminen palvelimelle
```bash
put tiedosto.txt
```

### Kaikkien tiedostojen listaaminen
```bash
ls
```

### Tiedostojen siirtäminen ilman vahvistusta
```bash
ftp -i ftp.example.com
```

## Vinkit
- Käytä `-v`-vaihtoehtoa, jos haluat nähdä tarkempia tietoja siirroista.
- Muista aina kirjautua ulos FTP-istunnosta komennolla `bye` tai `quit`.
- Varmista, että käytät turvallista yhteyttä, kuten SFTP:tä, jos mahdollista, koska FTP ei salaa tietoja.