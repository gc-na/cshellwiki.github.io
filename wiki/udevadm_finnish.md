# [Linux] Bash udevadm käyttö: Laitehallinnan komento

## Yleiskatsaus
`udevadm` on komento, jota käytetään Linux-järjestelmissä laitteiden hallintaan ja tiedon keräämiseen udev-järjestelmästä. Se mahdollistaa laitteiden tunnistamisen, konfiguroinnin ja tilan tarkistamisen.

## Käyttö
Perussyntaksi `udevadm`-komennolle on seuraava:

```bash
udevadm [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `info`: Näyttää tietoja laitteesta.
- `trigger`: Käynnistää udev-säännöt manuaalisesti.
- `settle`: Odottaa, että kaikki laitteet on tunnistettu.
- `control`: Hallitsee udev-prosessin toimintaa.

## Yleiset esimerkit

### 1. Laiteinformaatio
Voit saada tietoa tietystä laitteesta käyttämällä sen nimeä tai polkua:

```bash
udevadm info --query=all --name=/dev/sda
```

### 2. Udev-sääntöjen laukaiseminen
Jos haluat laukaista udev-säännöt manuaalisesti, voit käyttää seuraavaa komentoa:

```bash
udevadm trigger
```

### 3. Laitehallinnan odottaminen
Jos haluat varmistaa, että kaikki laitteet on tunnistettu ennen jatkamista, käytä:

```bash
udevadm settle
```

### 4. Udev-prosessin hallinta
Voit hallita udev-prosessia seuraavalla komennolla:

```bash
udevadm control --reload-rules
```

## Vinkit
- Käytä `udevadm monitor` -komentoa seurataksesi laitteiden tapahtumia reaaliajassa.
- Varmista, että sinulla on tarvittavat oikeudet suorittaa `udevadm`-komento, erityisesti laitehallintaan liittyvissä toiminnoissa.
- Hyödynnä `--help`-vaihtoehtoa saadaksesi lisätietoja ja vaihtoehtoja, joita voit käyttää komennossa.