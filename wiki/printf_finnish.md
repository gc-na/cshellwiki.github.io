# [Linux] Bash printf käyttö: Tulostaa muotoiltua tekstiä

## Yleiskatsaus
`printf`-komento on Bashissa käytettävä työkalu, joka mahdollistaa muotoillun tekstin tulostamisen. Se on erityisen hyödyllinen, kun halutaan hallita tarkasti, miltä tulostettu teksti näyttää, kuten numeroiden desimaalit, merkkijonojen pituudet ja muut muotoiluvaihtoehdot.

## Käyttö
Perussyntaksi `printf`-komennolle on seuraava:

```bash
printf [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-v`: Tallentaa tulosteen muuttujaan sen sijaan, että tulostaisi sen suoraan.
- `%s`: Merkkijonomuotoilu.
- `%d`: Kokonaisluku.
- `%f`: Liukuluku.
- `%x`: Kuudenteen muotoon (heksadesimaalimuoto).

## Yleiset esimerkit
### Esimerkki 1: Yksinkertainen merkkijonon tulostus
```bash
printf "Hei, maailma!\n"
```

### Esimerkki 2: Kokonaisluvun tulostus
```bash
printf "Luku: %d\n" 42
```

### Esimerkki 3: Liukuluvun tulostus tietyllä tarkkuudella
```bash
printf "Pi on noin: %.2f\n" 3.14159
```

### Esimerkki 4: Useiden arvojen tulostus
```bash
printf "Nimi: %s, Ikä: %d\n" "Matti" 30
```

### Esimerkki 5: Muuttujan käyttö
```bash
nimi="Liisa"
printf "Tervetuloa, %s!\n" "$nimi"
```

## Vinkit
- Käytä `\n` rivinvaihtoa tulostuksessa, jotta tulostus on selkeämpi.
- Muista, että `printf` ei lisää automaattisesti rivinvaihtoa, joten lisää se tarvittaessa.
- Hyödynnä muotoiluvaihtoehtoja tarkkuuden ja esitystavan hallintaan, erityisesti numeroiden kanssa.