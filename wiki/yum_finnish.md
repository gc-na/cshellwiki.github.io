# [Linux] Bash yum käyttö: Pakettien hallinta

## Yleiskatsaus
`yum` (Yellowdog Updater, Modified) on pakettien hallintatyökalu, jota käytetään Red Hat -perustaisissa Linux-jakeluissa, kuten CentOS ja Fedora. Se mahdollistaa ohjelmistopakettien asentamisen, päivittämisen ja poistamisen helposti komentoriviltä.

## Käyttö
Perussyntaksi `yum`-komennolle on seuraava:

```bash
yum [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `install`: Asentaa halutun ohjelmistopaketin.
- `remove`: Poistaa halutun ohjelmistopaketin.
- `update`: Päivittää asennetut paketit uusimpiin saatavilla oleviin versioihin.
- `list`: Näyttää saatavilla olevat tai asennetut paketit.
- `search`: Etsii paketteja nimellä tai kuvauksella.

## Yleiset esimerkit
Asennetaan ohjelmistopaketti:
```bash
yum install paketin_nimi
```

Poistetaan ohjelmistopaketti:
```bash
yum remove paketin_nimi
```

Päivitetään kaikki asennetut paketit:
```bash
yum update
```

Näytetään kaikki saatavilla olevat paketit:
```bash
yum list available
```

Etsitään paketteja:
```bash
yum search hakusana
```

## Vinkit
- Käytä `yum clean all` -komentoa tyhjentääksesi välimuistin, mikä voi auttaa ratkaisemaan ongelmia pakettien asennuksessa.
- Tarkista aina, mitä päivityksiä ollaan tekemässä, ennen kuin suoritat `yum update` -komennon, jotta tiedät, mitkä paketit muuttuvat.
- Hyödynnä `yum info paketin_nimi` -komentoa saadaksesi lisätietoja tietystä paketista ennen sen asentamista tai poistamista.