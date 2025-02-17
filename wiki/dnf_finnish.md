# [Linux] Bash dnf käyttö: Pakettien hallinta

## Yleiskatsaus
`dnf` (Dandified YUM) on pakettien hallintatyökalu, jota käytetään Red Hat -perustaisissa Linux-jakeluissa, kuten Fedora ja CentOS. Se mahdollistaa ohjelmistopakettien asentamisen, päivittämisen ja poistamisen helposti komentoriviltä.

## Käyttö
Perussyntaksi `dnf`-komennolle on seuraava:

```bash
dnf [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `install`: Asentaa yhden tai useamman paketin.
- `remove`: Poistaa yhden tai useamman paketin.
- `update`: Päivittää asennetut paketit uusimpiin versioihin.
- `search`: Etsii paketteja nimen tai kuvauksen perusteella.
- `info`: Näyttää tietoja tietystä paketista.

## Yleiset esimerkit
### Paketin asentaminen
Asentaaksesi esimerkiksi `vim`-editorin, käytä seuraavaa komentoa:

```bash
dnf install vim
```

### Paketin poistaminen
Poistaaksesi `vim`-editorin, käytä:

```bash
dnf remove vim
```

### Pakettien päivittäminen
Päivittääksesi kaikki asennetut paketit, käytä:

```bash
dnf update
```

### Paketin etsiminen
Etsi paketteja, jotka sisältävät sanan "httpd":

```bash
dnf search httpd
```

### Pakettitietojen näyttäminen
Näytä tietoja `httpd`-paketista:

```bash
dnf info httpd
```

## Vinkit
- Käytä `dnf`-komentoa `--assumeyes`-vaihtoehdolla, jos haluat automaattisesti hyväksyä kaikki kyselyt, esimerkiksi: `dnf install vim --assumeyes`.
- Tarkista säännöllisesti päivitykset komennolla `dnf update` varmistaaksesi, että järjestelmäsi on ajan tasalla.
- Hyödynnä `dnf history`-komentoa nähdäksesi aikaisemmat asennukset ja päivitykset, mikä voi auttaa ongelmatilanteissa.