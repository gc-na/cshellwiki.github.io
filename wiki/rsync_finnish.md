# [Linux] Bash rsync käyttö: Tiedostojen synkronointi ja siirto

## Overview
Rsync on tehokas työkalu tiedostojen ja hakemistojen synkronointiin ja siirtoon paikallisesti tai etäpalvelimille. Se mahdollistaa tiedostojen kopioimisen vain muutoksista, mikä tekee siitä nopean ja kaikin puolin tehokkaan.

## Usage
Perussyntaksi rsync-komennolle on seuraava:

```bash
rsync [options] [arguments]
```

## Common Options
- `-a` : Arkistointitila, joka säilyttää tiedostojen ominaisuudet (oikeudet, aikaleimat jne.).
- `-v` : Näyttää yksityiskohtaisen tulosteen siirrettävistä tiedostoista.
- `-z` : Pakkaa tiedostot siirron aikana, mikä voi nopeuttaa siirtoa erityisesti hitailla yhteyksillä.
- `-r` : Kopioi hakemistot rekursiivisesti.
- `--delete` : Poistaa kohdekansiosta tiedostot, joita ei ole lähdekansiossa.

## Common Examples

### Esimerkki 1: Tiedostojen kopioiminen paikallisesti
Kopioi tiedosto `file.txt` hakemistosta `source` hakemistoon `destination`:

```bash
rsync -av source/file.txt destination/
```

### Esimerkki 2: Hakemiston synkronointi etäpalvelimelle
Synkronoi paikallinen hakemisto `local_dir` etäpalvelimen hakemistoon `remote_dir`:

```bash
rsync -avz local_dir/ user@remote_host:/path/to/remote_dir/
```

### Esimerkki 3: Hakemiston synkronointi ja poistaminen
Synkronoi hakemisto ja poista kohdekansiosta ylimääräiset tiedostot:

```bash
rsync -av --delete local_dir/ user@remote_host:/path/to/remote_dir/
```

## Tips
- Käytä `-n` (dry run) -optiota testataksesi, mitä rsync tekisi ilman todellista siirtoa.
- Varmista, että käytät oikeita polkuja, erityisesti etäpalvelimilla, jotta vältät vahingossa tapahtuvan tiedostojen menetyksen.
- Hyödynnä SSH-yhteyttä turvallisten siirtojen varmistamiseksi etäpalvelimille.