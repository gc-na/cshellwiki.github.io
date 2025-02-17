# [Linux] Bash vgextend käyttö: Laajentaa loogista volyymiä

## Overview
`vgextend` on komento, jota käytetään Linux-järjestelmissä laajentamaan loogista volyymiä (Volume Group, VG) lisäämällä siihen uusia fyysisiä levyjä (Physical Volumes, PV). Tämä mahdollistaa tallennustilan lisäämisen olemassa olevaan loogiseen volyymiin, mikä on erityisen hyödyllistä, kun tilaa tarvitaan lisää.

## Usage
Perussyntaksi `vgextend`-komennolle on seuraava:

```bash
vgextend [options] [arguments]
```

## Common Options
- `-l, --extents <number>`: Määrittää laajennettavien laajennusten (extents) määrän.
- `-n, --no-resize`: Estää loogisen volyymin automaattisen koon muutoksen.
- `-v, --verbose`: Näyttää lisätietoja komennon suorittamisesta.
- `--test`: Suorittaa testin ilman muutosten tekemistä.

## Common Examples
### Esimerkki 1: Uuden fyysisen levyn lisääminen
Lisätään uusi fyysinen levy nimeltä `/dev/sdb` loogiseen volyymiin nimeltä `vg1`.

```bash
vgextend vg1 /dev/sdb
```

### Esimerkki 2: Useiden levyjen lisääminen
Voit myös lisätä useita levyjä kerralla. Esimerkiksi:

```bash
vgextend vg1 /dev/sdb /dev/sdc
```

### Esimerkki 3: Laajennettavien laajennusten määrittäminen
Jos haluat määrittää laajennettavien laajennusten määrän, voit käyttää seuraavaa komentoa:

```bash
vgextend -l +5 vg1 /dev/sdd
```

## Tips
- Varmista, että fyysiset levyt, jotka aiot lisätä, on alustettu ja ne ovat käytettävissä.
- Ennen `vgextend`-komennon suorittamista on hyvä tarkistaa nykyinen loogisen volyymin tila komennolla `vgs`.
- Käytä `--test`-optiota ennen varsinaista suorittamista varmistaaksesi, että kaikki on kunnossa.