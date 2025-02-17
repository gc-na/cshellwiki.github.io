# [Linux] Bash case käyttö: Ehtojen tarkistaminen

## Overview
`case`-komento Bashissa on tehokas tapa tarkistaa ja käsitellä useita ehtoja. Se mahdollistaa erilaisten vaihtoehtojen vertaamisen syötteeseen ja suorittaa vastaavat komennot, mikä tekee siitä hyödyllisen skriptien hallinnassa.

## Usage
Perussyntaksi `case`-komennolle on seuraava:

```bash
case [muuttuja] in
    [kuvio1])
        [toimenpide1]
        ;;
    [kuvio2])
        [toimenpide2]
        ;;
    *)
        [oletustoimenpide]
        ;;
esac
```

## Common Options
- `*`: Käytetään oletuskuvioon, jos mikään muu ei täsmää.
- `;;`: Merkitsee, että nykyinen tapaus on päättynyt.
- `esac`: Merkitsee `case`-rakenteen loppua.

## Common Examples

### Esimerkki 1: Yksinkertainen ehtotarkistus
```bash
case $1 in
    "kissa")
        echo "Sinulla on kissa."
        ;;
    "koira")
        echo "Sinulla on koira."
        ;;
    *)
        echo "Sinulla on jokin muu eläin."
        ;;
esac
```

### Esimerkki 2: Useita vaihtoehtoja
```bash
case $1 in
    "punainen" | "sininen" | "vihreä")
        echo "Valitsit värin."
        ;;
    "kissa" | "koira")
        echo "Valitsit eläimen."
        ;;
    *)
        echo "Valinta ei ole tunnettu."
        ;;
esac
```

### Esimerkki 3: Numerot ja merkkijonot
```bash
case $1 in
    [0-9])
        echo "Syötit numeron."
        ;;
    *)
        echo "Syötit merkkijonon."
        ;;
esac
```

## Tips
- Käytä `case`-komentoa, kun sinulla on useita ehtoja, joita haluat tarkistaa, sillä se tekee koodista selkeämpää ja helpommin luettavaa.
- Muista aina sulkea jokainen tapaus `;;`-merkillä, jotta Bash ymmärtää, että tapaus on päättynyt.
- Hyödynnä vaihtoehtojen yhdistämistä (esim. `|`) helpottaaksesi koodin kirjoittamista ja vähentääksesi toistoa.