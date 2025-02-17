# [Linux] Bash foreach käyttö: Toistaa komentoja useille arvoille

## Yleiskatsaus
`foreach`-komento on käytettävissä tietyissä Unix-pohjaisissa ympäristöissä, kuten C-shellissä, ja se mahdollistaa komennon suorittamisen useille arvoille tai muuttujille. Tämä komento on hyödyllinen, kun halutaan toistaa sama toiminto useille syötteille ilman, että tarvitsisi kirjoittaa samaa komentoa useaan kertaan.

## Käyttö
Perussyntaksi `foreach`-komennolle on seuraava:

```
foreach [muuttuja] (lista)
    komento
end
```

## Yleiset vaihtoehdot
- `muuttuja`: Määrittelee nimen, jota käytetään silmukassa.
- `lista`: Lista arvoista, joille komento suoritetaan.
- `komento`: Komento, joka suoritetaan jokaiselle listan arvolle.

## Yleiset esimerkit

### Esimerkki 1: Tiedostojen nimeäminen
```bash
foreach i (file1 file2 file3)
    echo "Käsittelen tiedostoa $i"
end
```

### Esimerkki 2: Komentojen suorittaminen
```bash
foreach i (1 2 3)
    echo "Numero: $i"
end
```

### Esimerkki 3: Tiedostojen poistaminen
```bash
foreach file (tiedosto1.txt tiedosto2.txt)
    rm $file
end
```

## Vinkit
- Varmista, että käytät oikeaa syntaksia, sillä virheellinen syntaksi voi aiheuttaa virheitä.
- Käytä `echo`-komentoa testataksesi silmukan toimivuutta ennen varsinaisten komentojen suorittamista.
- Muista, että `foreach`-komento ei ole Bashin natiivi komento, joten se saattaa olla käytettävissä vain tietyissä ympäristöissä, kuten C-shellissä. Bashissa vastaava toiminto voidaan toteuttaa `for`-silmukalla.