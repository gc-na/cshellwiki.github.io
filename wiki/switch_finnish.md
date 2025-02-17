# [Linux] Bash switch käyttö: Vaihtoehtojen hallinta

## Yleiskatsaus
`switch`-komento on Bashin komento, jota käytetään vaihtoehtojen hallintaan ja valintojen tekemiseen skripteissä. Se mahdollistaa erilaisten ehtojen tarkistamisen ja niiden perusteella erilaisten toimintojen suorittamisen.

## Käyttö
Perussyntaksi `switch`-komennolle on seuraava:

```bash
switch [options] [arguments]
```

## Yleiset vaihtoehdot
- `-e`: Määrittää, että komento suoritetaan vain, jos ehto on tosi.
- `-d`: Käytetään oletusarvon määrittämiseen, jos mikään muu ehto ei täyty.
- `-h`: Näyttää ohjeet ja käytön.

## Yleiset esimerkit
### Esimerkki 1: Perusvalinta
```bash
switch $1 in
    "option1")
        echo "Valitsit vaihtoehdon 1"
        ;;
    "option2")
        echo "Valitsit vaihtoehdon 2"
        ;;
    *)
        echo "Tuntematon vaihtoehto"
        ;;
esac
```

### Esimerkki 2: Oletusarvo
```bash
switch $1 in
    "yes")
        echo "Vastaus on kyllä"
        ;;
    "no")
        echo "Vastaus on ei"
        ;;
    *)
        echo "Oletusarvo: ei tiedossa"
        ;;
esac
```

### Esimerkki 3: Useita ehtoja
```bash
switch $1 in
    "start")
        echo "Käynnistetään ohjelma"
        ;;
    "stop")
        echo "Pysäytetään ohjelma"
        ;;
    "restart")
        echo "Käynnistetään ohjelma uudelleen"
        ;;
    *)
        echo "Tuntematon komento"
        ;;
esac
```

## Vinkit
- Käytä `-h`-vaihtoehtoa saadaksesi lisätietoja komennosta.
- Muista aina sulkea `switch`-komento `esac`-avainsanalla.
- Testaa komento huolellisesti, jotta voit varmistaa, että kaikki vaihtoehdot toimivat odotetusti.