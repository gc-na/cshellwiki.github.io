# [Linux] Bash chmod käyttö: Tiedostojen käyttöoikeuksien hallinta

## Yleiskatsaus
`chmod`-komento (change mode) on käytössä Unix- ja Linux-järjestelmissä tiedostojen ja hakemistojen käyttöoikeuksien muokkaamiseen. Sen avulla voit määrittää, kuka voi lukea, kirjoittaa tai suorittaa tiettyjä tiedostoja.

## Käyttö
Perussyntaksi `chmod`-komennolle on seuraava:

```bash
chmod [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `u`: Käyttäjä (omistaja)
- `g`: Ryhmä
- `o`: Muut käyttäjät
- `a`: Kaikki (u, g, o)
- `+`: Lisää oikeus
- `-`: Poistaa oikeus
- `=`: Määrittelee oikeuden tarkasti

## Yleiset esimerkit
1. **Anna omistajalle kirjoitusoikeus tiedostolle:**
   ```bash
   chmod u+w tiedosto.txt
   ```

2. **Poista suoritusoikeus muilta käyttäjiltä:**
   ```bash
   chmod o-x tiedosto.sh
   ```

3. **Anna kaikille lukuoikeus hakemistolle:**
   ```bash
   chmod a+r hakemisto/
   ```

4. **Määritä tarkat oikeudet tiedostolle (omistajalle luku- ja kirjoitusoikeus, muille vain lukuoikeus):**
   ```bash
   chmod 644 tiedosto.txt
   ```

5. **Anna suoritusoikeus kaikille tiedostolle:**
   ```bash
   chmod a+x ohjelma
   ```

## Vinkit
- Käytä `ls -l`-komentoa tarkistaaksesi tiedostojen nykyiset käyttöoikeudet ennen muutoksia.
- Ole varovainen käyttöoikeuksien myöntämisessä, erityisesti suoritusoikeuksien kanssa, jotta vältät turvallisuusongelmia.
- Voit käyttää `-R`-vaihtoehtoa muuttaaksesi käyttöoikeuksia rekursiivisesti hakemistossa:
  ```bash
  chmod -R 755 hakemisto/
  ```