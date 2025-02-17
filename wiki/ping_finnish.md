# [Linux] Bash ping käyttö: Verkkoyhteyden tarkistaminen

## Yleiskatsaus
Ping-komento on työkalu, jota käytetään verkkoyhteyden testaamiseen ja viiveen mittaamiseen. Se lähettää ICMP-echo-pyyntöjä kohteelle ja odottaa vastauksia, mikä auttaa selvittämään, onko kohde saavutettavissa ja kuinka nopeasti se vastaa.

## Käyttö
Perussyntaksi ping-komennolle on seuraava:

```bash
ping [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-c [luku]`: Määrittää, kuinka monta pyyntöä lähetetään.
- `-i [sekunnit]`: Asettaa viiveen pyyntöjen välillä.
- `-t [luku]`: Määrittää aikarajan (time to live) paketeille.
- `-s [luku]`: Määrittää lähetettävän datan koon tavuina.

## Yleiset esimerkit
1. **Perus ping-komento**:
   ```bash
   ping google.com
   ```

2. **Pingaa tietty määrä kertoja**:
   ```bash
   ping -c 4 google.com
   ```

3. **Aseta viive pyyntöjen välillä**:
   ```bash
   ping -i 2 google.com
   ```

4. **Pingaa ja määritä datan koko**:
   ```bash
   ping -s 64 google.com
   ```

## Vinkit
- Käytä `-c`-vaihtoehtoa, jos haluat rajoittaa pyyntöjen määrää, jotta et jää ping-komentoon ikuisesti.
- Ping-komento on hyödyllinen myös verkon ongelmien diagnosoinnissa; jos et saa vastauksia, tarkista verkkoyhteytesi.
- Voit käyttää `Ctrl + C` keskeyttääksesi ping-komennon, jos se on käynnissä jatkuvasti.