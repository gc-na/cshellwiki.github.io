# [Linux] Bash usermod käyttö: Käyttäjätietojen muokkaaminen

## Yleiskatsaus
usermod-komento on työkalu, jota käytetään käyttäjätilien muokkaamiseen Linux-järjestelmässä. Sen avulla voit päivittää käyttäjätietoja, kuten ryhmiä, kotihakemistoja ja muita asetuksia.

## Käyttö
Perussyntaksi usermod-komennolle on seuraava:

```bash
usermod [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-aG`: Lisää käyttäjä tiettyyn ryhmään ilman, että hänet poistetaan muista ryhmistä.
- `-d`: Määrittää käyttäjän uuden kotihakemiston.
- `-l`: Muuttaa käyttäjän nimeä.
- `-s`: Määrittää käyttäjän oletuskuoren.
- `-u`: Muuttaa käyttäjän UID:tä.

## Yleiset esimerkit
- Lisää käyttäjä `john` ryhmään `sudo`:
    ```bash
    usermod -aG sudo john
    ```

- Muuta käyttäjän `anna` kotihakemisto ` /home/anna_new`:
    ```bash
    usermod -d /home/anna_new anna
    ```

- Muuta käyttäjän `mike` käyttäjänimeä `michael`:
    ```bash
    usermod -l michael mike
    ```

- Aseta käyttäjän `sara` oletuskuoreksi `/bin/bash`:
    ```bash
    usermod -s /bin/bash sara
    ```

- Muuta käyttäjän `bob` UID:tä `1050`:
    ```bash
    usermod -u 1050 bob
    ```

## Vinkit
- Varmista, että käytät `-aG`-vaihtoehtoa, kun lisäät käyttäjiä ryhmiin, jotta et poista heitä muista ryhmistä.
- Tarkista aina käyttäjän tiedot komennolla `id [käyttäjänimi]` ennen ja jälkeen muutosten varmistaaksesi, että ne on tehty oikein.
- Käytä `usermod`-komentoa vain root-oikeuksilla tai sudo-käyttäjänä, jotta voit tehdä tarvittavat muutokset.