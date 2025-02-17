# [Linux] Bash lsmod käyttö: Näyttää ladatut moduulit

## Yleiskatsaus
`lsmod` on komento, joka näyttää nykyiset ladatut ydinmoduulit Linux-järjestelmässä. Se listaa moduulit, niiden koon ja riippuvuudet, mikä auttaa käyttäjiä ymmärtämään, mitkä moduulit ovat aktiivisia ja käytössä.

## Käyttö
Perussyntaksi `lsmod`-komennolle on seuraava:

```bash
lsmod [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-h`, `--help`: Näyttää apuviestin ja käytön.
- `-v`, `--verbose`: Näyttää lisätietoja ladatuista moduuleista.

## Yleiset esimerkit
### 1. Ladattujen moduulien listaaminen
Voit listata kaikki ladatut moduulit yksinkertaisesti kirjoittamalla:

```bash
lsmod
```

### 2. Apua komennolle
Jos tarvitset apua `lsmod`-komennon käytössä, voit käyttää seuraavaa komentoa:

```bash
lsmod --help
```

### 3. Yksityiskohtaisempi näkymä
Jos haluat nähdä lisätietoja moduuleista, voit käyttää verbose-vaihtoehtoa:

```bash
lsmod -v
```

## Vinkit
- Käytä `lsmod`-komentoa yhdessä muiden komentojen, kuten `modinfo`, kanssa saadaksesi lisätietoja moduuleista.
- Tarkista säännöllisesti ladattujen moduulien lista varmistaaksesi, että järjestelmässä ei ole tarpeettomia moduuleja, jotka voivat vaikuttaa suorituskykyyn.
- Muista, että `lsmod` ei vaadi erityisiä oikeuksia, joten voit käyttää sitä tavallisena käyttäjänä.