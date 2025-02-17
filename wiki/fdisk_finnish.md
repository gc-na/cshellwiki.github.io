# [Linux] Bash fdisk käyttö: Levyn osioiden hallinta

## Yleiskatsaus
`fdisk` on komentorivipohjainen työkalu, jota käytetään levyosion hallintaan Linux-järjestelmissä. Sen avulla voit luoda, poistaa ja muokata osioita kiintolevyillä ja muilla tallennuslaitteilla.

## Käyttö
Perussyntaksi `fdisk`-komennolle on seuraava:

```bash
fdisk [vaihtoehdot] [argumentit]
```

## Yhteiset vaihtoehdot
- `-l`: Listaa kaikki levyosiot.
- `-u`: Käyttää osioiden kokoa sektoreina.
- `-n`: Luo uusi osio.
- `-d`: Poistaa olemassa olevan osion.
- `-t`: Muuttaa osion tiedostojärjestelmän tyyppiä.

## Yhteiset esimerkit
### Levyosioiden listaaminen
Voit listata kaikki käytettävissä olevat levyosiot komennolla:

```bash
fdisk -l
```

### Uuden osion luominen
Uuden osion luomiseksi voit käyttää seuraavaa komentoa:

```bash
fdisk /dev/sda
```
Tämän jälkeen seuraa ohjeita uuden osion määrittämiseksi.

### Olemassa olevan osion poistaminen
Jos haluat poistaa osion, käytä seuraavaa komentoa:

```bash
fdisk /dev/sda
```
Valitse sitten `d` ja määritä poistettavan osion numero.

### Osion tiedostojärjestelmän tyypin muuttaminen
Voit muuttaa osion tiedostojärjestelmän tyyppiä seuraavalla komennolla:

```bash
fdisk /dev/sda
```
Valitse `t` ja syötä osion numero sekä uusi tiedostojärjestelmän tyyppi.

## Vinkit
- Varmista, että sinulla on varmuuskopiot tärkeistä tiedoista ennen osioiden muokkaamista.
- Käytä `man fdisk` saadaksesi lisätietoja ja ohjeita komennon käytöstä.
- Ole varovainen osioiden poistamisessa, sillä se voi johtaa tietojen menetykseen.