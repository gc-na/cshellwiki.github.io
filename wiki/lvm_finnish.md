# [Linux] Bash lvm käyttö: Loogisten volyymien hallinta

## Yleiskatsaus
`lvm` (Logical Volume Manager) on työkalu, joka mahdollistaa loogisten volyymien hallinnan Linux-järjestelmissä. Sen avulla voit luoda, muokata ja hallita loogisia volyymejä, mikä helpottaa levytilan hallintaa ja joustavuutta.

## Käyttö
Perussyntaksi `lvm`-komennolle on seuraava:

```bash
lvm [options] [arguments]
```

## Yleiset vaihtoehdot
- `create`: Luo uuden loogisen volyymin.
- `remove`: Poistaa olemassa olevan loogisen volyymin.
- `extend`: Laajentaa olemassa olevaa loogista volyymiä.
- `reduce`: Vähentää olemassa olevan loogisen volyymin kokoa.
- `lvdisplay`: Näyttää loogisten volyymien tiedot.

## Yleiset esimerkit
### Loogisen volyymin luominen
```bash
lvcreate -n uusi_volyymi -L 10G ryhmä
```
Tämä komento luo uuden loogisen volyymin nimeltä `uusi_volyymi`, jonka koko on 10 Gt, määritellyssä ryhmässä.

### Loogisen volyymin poistaminen
```bash
lvremove /dev/ryhmä/uusi_volyymi
```
Tämä komento poistaa loogisen volyymin `uusi_volyymi`.

### Loogisen volyymin laajentaminen
```bash
lvextend -L +5G /dev/ryhmä/uusi_volyymi
```
Tämä komento laajentaa loogista volyymiä `uusi_volyymi` viidellä gigatavulla.

### Loogisen volyymin koon vähentäminen
```bash
lvreduce -L -5G /dev/ryhmä/uusi_volyymi
```
Tämä komento vähentää loogisen volyymin kokoa viidellä gigatavulla.

### Loogisten volyymien tietojen näyttäminen
```bash
lvdisplay
```
Tämä komento näyttää kaikki loogiset volyymit ja niiden tiedot.

## Vinkit
- Varmista aina, että olet varmuuskopioinut tärkeät tiedot ennen loogisten volyymien muokkaamista.
- Käytä `lvdisplay`-komentoa säännöllisesti tarkistaaksesi loogisten volyymien tilan.
- Suunnittele loogisten volyymien koko ja rakenne etukäteen, jotta voit välttää tarpeettomia muutoksia tulevaisuudessa.