# [Linux] Bash pacman käyttö: Pakettien hallinta Arch Linuxissa

## Yleiskatsaus
Pacman on Arch Linuxin pakettien hallintatyökalu, joka mahdollistaa ohjelmistojen asentamisen, päivittämisen ja poistamisen. Se hallitsee paketteja binäärimuodossa ja tarjoaa tehokkaan tavan hallita järjestelmän ohjelmistoja.

## Käyttö
Perussyntaksi pacman-komennolle on seuraava:
```bash
pacman [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-S`: Asentaa paketin.
- `-R`: Poistaa paketin.
- `-U`: Asentaa paketin paikallisesta tiedostosta.
- `-Sy`: Päivittää pakettitietokannan.
- `-Su`: Päivittää kaikki asennetut paketit.
- `-Q`: Kysyy tietoja asennetuista paketeista.

## Yleiset esimerkit
Asennetaan ohjelma:
```bash
pacman -S ohjelman_nimi
```

Poistetaan ohjelma:
```bash
pacman -R ohjelman_nimi
```

Päivitetään kaikki asennetut paketit:
```bash
pacman -Su
```

Asennetaan paketti paikallisesta tiedostosta:
```bash
pacman -U /polku/pakettiin.pkg.tar.zst
```

Katsotaan asennettujen pakettien lista:
```bash
pacman -Q
```

## Vinkit
- Käytä `-Syu` yhdistääksesi pakettitietokannan päivittämisen ja kaikkien pakettien päivittämisen yhteen komentoihin.
- Tarkista aina, mitä paketteja ollaan poistamassa `-R`-vaihtoehdolla, jotta et vahingossa poista tärkeitä riippuvuuksia.
- Hyödynnä `pacman -Ss hakusana` etsiäksesi paketteja, jotka sisältävät tietyn hakusanan.