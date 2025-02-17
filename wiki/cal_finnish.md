# [Linux] Bash cal käyttö: Näyttää kalenterin

## Overview
`cal`-komento näyttää kuukausittaisen kalenterin komentorivillä. Se on hyödyllinen työkalu, jolla voit nopeasti tarkistaa päivämäärät ja viikonpäivät ilman graafista käyttöliittymää.

## Usage
Perussyntaksi `cal`-komennolle on seuraava:

```bash
cal [options] [arguments]
```

## Common Options
- `-m`: Näyttää kalenterin maanantaista sunnuntaihin.
- `-y`: Näyttää koko vuoden kalenterin.
- `-3`: Näyttää nykyisen kuukauden, edellisen ja seuraavan kuukauden.
- `-j`: Näyttää päivämäärät vuodenpäivinä.
- `-h`: Näyttää kalenterin ilman ykköspäivää.

## Common Examples
### Nykyisen kuukauden kalenteri
```bash
cal
```

### Tämän vuoden kalenteri
```bash
cal -y
```

### Kolme kuukautta (nykyinen, edellinen ja seuraava)
```bash
cal -3
```

### Kalenteri, jossa viikko alkaa maanantaista
```bash
cal -m
```

### Kalenteri, jossa päivämäärät ovat vuodenpäivinä
```bash
cal -j
```

## Tips
- Voit yhdistää `cal`-komennon muihin komentoihin, kuten `grep`, etsiäksesi tiettyjä päivämääriä tai tapahtumia.
- Käytä `man cal` saadaksesi lisätietoja ja kaikkia käytettävissä olevia vaihtoehtoja.