# [Linux] Bash umask käyttö: Tiedostojen oletusoikeuksien määrittäminen

## Yleiskatsaus
`umask`-komento määrittää oletusoikeudet uusille tiedostoille ja hakemistoille, jotka luodaan käyttäjän toimesta. Se määrittää, mitkä oikeudet poistetaan tiedostojen ja hakemistojen oletusoikeuksista.

## Käyttö
Perussyntaksi `umask`-komennolle on seuraava:

```bash
umask [options] [arguments]
```

## Yleiset vaihtoehdot
- `-S`: Näyttää umaskin symbolisessa muodossa.
- `-p`: Näyttää nykyisen umask-arvon.
- `-c`: Muuttaa umask-arvoa ja näyttää sen jälkeen.

## Yleiset esimerkit
1. **Nykyisen umask-arvon tarkistaminen**:
   ```bash
   umask
   ```

2. **Umask-arvon asettaminen**:
   Asetetaan umask-arvoksi 022, jolloin uusien tiedostojen oletusoikeudet ovat 644 ja hakemistojen 755.
   ```bash
   umask 022
   ```

3. **Umask-arvon näyttäminen symbolisessa muodossa**:
   ```bash
   umask -S
   ```

4. **Umask-arvon tarkistaminen ja asettaminen**:
   Tarkista nykyinen umask ja aseta se 027:ksi.
   ```bash
   umask -p
   umask 027
   ```

## Vinkit
- Muista, että umask-arvo vaikuttaa vain uusiin tiedostoihin ja hakemistoihin, ei olemassa oleviin.
- Aseta umask-arvo käyttäjäprofiilissasi (esim. `.bashrc` tai `.bash_profile`), jotta se pysyy voimassa myös uudelleenkäynnistyksen jälkeen.
- Käytä umaskia varovaisesti, erityisesti palvelimilla, joissa tiedostojen oikeudet ovat kriittisiä tietoturvan kannalta.