# [Linux] Bash sftp käyttö: Tiedostojen siirtäminen turvallisesti

## Yleiskatsaus
`sftp` (Secure File Transfer Protocol) on komentorivipohjainen työkalu, jota käytetään tiedostojen siirtämiseen turvallisesti SSH-yhteyden yli. Se tarjoaa käyttäjille mahdollisuuden ladata ja ladata tiedostoja etäpalvelimilta turvallisella tavalla.

## Käyttö
Perussyntaksi `sftp`-komennolle on seuraava:

```bash
sftp [options] [user@]host
```

## Yleiset vaihtoehdot
- `-P port`: Määrittää käytettävän portin (oletus on 22).
- `-o option`: Määrittää SSH-yhteyden vaihtoehtoja, kuten `IdentityFile` tai `StrictHostKeyChecking`.
- `-b batchfile`: Suorittaa komennot, jotka on määritetty erätiedostossa.

## Yleiset esimerkit
### Yhdistäminen etäpalvelimeen
Yhdistä etäpalvelimeen käyttäen käyttäjänimeä:

```bash
sftp user@hostname
```

### Tiedoston lataaminen etäpalvelimelta
Lataa tiedosto etäpalvelimelta paikalliseen hakemistoon:

```bash
sftp user@hostname:/path/to/remote/file /path/to/local/directory
```

### Tiedoston lähettäminen paikalliselta koneelta etäpalvelimelle
Lähetä tiedosto paikalliselta koneelta etäpalvelimelle:

```bash
sftp user@hostname
put /path/to/local/file /path/to/remote/directory
```

### Tiedostojen listaaminen etäpalvelimella
Listaa tiedostot etäpalvelimen hakemistossa:

```bash
sftp user@hostname
ls /path/to/remote/directory
```

## Vinkit
- Varmista, että SSH-yhteys toimii ennen `sftp`-komennon käyttöä.
- Käytä `-b`-vaihtoehtoa, jos haluat suorittaa useita komentoja automaattisesti erätiedostosta.
- Hyödynnä `get` ja `put` -komentoja tiedostojen siirtämiseen nopeasti etäpalvelimen ja paikallisen koneen välillä.