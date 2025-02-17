# [Linux] Bash killall käyttö: Prosessien lopettaminen nimellä

## Yleiskatsaus
`killall`-komento käytetään prosessien lopettamiseen niiden nimen perusteella. Se on hyödyllinen työkalu, kun haluat sulkea useita samannimisiä prosesseja yhdellä komennolla.

## Käyttö
Perussyntaksi `killall`-komennolle on seuraava:

```bash
killall [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-u, --user <käyttäjä>`: Lopettaa vain tietyn käyttäjän prosessit.
- `-q, --quiet`: Ei tulosta mitään, ellei virheitä esiinny.
- `-I, --ignore-case`: Ohittaa kirjainkoolla, eli se ei erota suuria ja pieniä kirjaimia.
- `-s, --signal <signaali>`: Määrittelee lähetettävän signaalin (oletus on SIGTERM).

## Yleiset esimerkit
- Kaikkien `firefox`-prosessien lopettaminen:

```bash
killall firefox
```

- Kaikkien `python`-prosessien lopettaminen:

```bash
killall python
```

- Tietyn käyttäjän `chrome`-prosessien lopettaminen:

```bash
killall -u käyttäjänimi chrome
```

- `gedit`-prosessien lopettaminen käyttäen SIGKILL-signaalia:

```bash
killall -s SIGKILL gedit
```

## Vinkit
- Varmista, että tiedät mitä prosesseja olet lopettamassa, jotta et vahingossa sulje tärkeitä ohjelmia.
- Käytä `-q`-vaihtoehtoa, jos et halua nähdä tulosteita onnistuneista lopetuksista.
- Tarkista prosessit ennen niiden lopettamista komennolla `ps aux | grep [prosessi]`, jotta voit varmistaa, että oikeat prosessit lopetetaan.