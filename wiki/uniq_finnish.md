# [Linux] Bash uniq käyttö: Poistaa peräkkäiset duplikaatit

## Yleiskatsaus
`uniq`-komento on Bashin työkalu, joka poistaa peräkkäiset duplikaatit tiedostosta tai syötteestä. Se on erityisen hyödyllinen, kun halutaan käsitellä tai analysoida tietoja, joissa on toistuvia rivejä.

## Käyttö
Perus syntaksi `uniq`-komennolle on seuraava:

```bash
uniq [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c`: Laskee ja näyttää kuinka monta kertaa kukin rivi esiintyy.
- `-d`: Näyttää vain ne rivit, jotka esiintyvät useita kertoja.
- `-u`: Näyttää vain ne rivit, jotka ovat ainutlaatuisia (esiintyvät vain kerran).
- `-i`: Ignoroi kirjainkoolla eroja vertailussa.

## Yleiset esimerkit
### Perus käyttö
Poista peräkkäiset duplikaatit tiedostosta `data.txt`:

```bash
uniq data.txt
```

### Laske duplikaatit
Laske ja näytä kuinka monta kertaa kukin rivi esiintyy:

```bash
uniq -c data.txt
```

### Näytä vain duplikaatit
Näytä vain ne rivit, jotka esiintyvät useita kertoja:

```bash
uniq -d data.txt
```

### Näytä vain ainutlaatuiset rivit
Näytä vain ne rivit, jotka ovat ainutlaatuisia:

```bash
uniq -u data.txt
```

## Vinkit
- Varmista, että syöte on lajiteltu ennen `uniq`-komennon käyttöä, jotta se toimii oikein. Voit käyttää `sort`-komentoa lajitellaksesi tiedoston ennen `uniq`-komentoa.
- Voit yhdistää `uniq`-komennon muihin komentoihin putkella, esimerkiksi: 

```bash
sort data.txt | uniq
```

- Käytä `-i`-vaihtoehtoa, jos haluat tehdä vertailuja, joissa kirjainkoolla ei ole merkitystä.