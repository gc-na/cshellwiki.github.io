# [Linux] Bash script käyttö: Tallenna komentorivitoimintoja

## Yleiskatsaus
`script`-komento on työkalu, joka tallentaa kaikki komentorivitoiminnot ja niiden tulosteet tiedostoon. Tämä on erityisen hyödyllistä, kun haluat dokumentoida työskentelysi tai jakaa komentorivitoimintojen tulokset myöhemmin.

## Käyttö
Perussyntaksi `script`-komennolle on seuraava:

```bash
script [vaihtoehdot] [tiedosto]
```

## Yleiset vaihtoehdot
- `-a`: Liittää tulosteen olemassa olevaan tiedostoon sen sijaan, että se ylikirjoittaisi sen.
- `-q`: Poistaa tulosteen näyttämisen komentorivillä, vain tiedostoon tallennus tapahtuu.
- `-t`: Tallentaa aikaleimat, jolloin voit nähdä, kuinka kauan kukin komento kesti.

## Yleiset esimerkit
### Perustallennus
Tallentaa kaikki komentorivitoiminnot `session.log`-tiedostoon:

```bash
script session.log
```

### Liittäminen olemassa olevaan tiedostoon
Liittää uuden sessiotaulun olemassa olevaan `session.log`-tiedostoon:

```bash
script -a session.log
```

### Hiljainen tila
Tallentaa komentorivitoiminnot ilman näyttöä komentorivillä:

```bash
script -q session.log
```

### Aikaleimojen tallentaminen
Tallentaa aikaleimat ja komentorivitoiminnot `timed_session.log`-tiedostoon:

```bash
script -t timed_session.log
```

## Vinkit
- **Käytä vaihtoehtoa `-q`**: Jos haluat keskittyä vain tallennukseen ilman häiriöitä, käytä hiljaista tilaa.
- **Tarkista tiedosto**: Muista tarkistaa tallennettu tiedosto varmistaaksesi, että kaikki tarvittavat komennot on tallennettu.
- **Käytä `exit`-komentoa**: Muista lopettaa `script`-sessio kirjoittamalla `exit`, jotta tiedosto sulkeutuu oikein.