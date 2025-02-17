# [Linux] Bash traceroute käyttö: Verkkoreittien jäljittäminen

## Yleiskatsaus
Traceroute-komento on työkalu, jota käytetään verkkoreittien jäljittämiseen tietokoneen ja kohdeosoitteen välillä. Se näyttää, kuinka monta reititintä (hop) paketti kulkee ennen kuin se saavuttaa määränpään, sekä kunkin reitittimen viiveen.

## Käyttö
Traceroute-komennon perussyntaksi on seuraava:

```bash
traceroute [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-m <max_hops>`: Määrittää maksimi reitittimien määrän, johon traceroute yrittää päästä.
- `-w <timeout>`: Asettaa aikarajan (sekunteina) jokaiselle reitittimelle.
- `-q <n>`: Määrittää, kuinka monta pakettia lähetetään jokaiselle reitittimelle (oletus on 3).
- `-I`: Käyttää ICMP ECHO -paketteja UDP-pakettien sijaan.

## Yleiset esimerkit
1. Perus traceroute komento:
   ```bash
   traceroute example.com
   ```

2. Määritä maksimi reitittimien määrä:
   ```bash
   traceroute -m 10 example.com
   ```

3. Aikarajan asettaminen:
   ```bash
   traceroute -w 2 example.com
   ```

4. ICMP-pakettien käyttäminen:
   ```bash
   traceroute -I example.com
   ```

## Vinkit
- Käytä `-m`-vaihtoehtoa, jos haluat rajoittaa reitittimien määrää ja nopeuttaa tulosten saamista.
- Tarkista, että sinulla on tarvittavat käyttöoikeudet, erityisesti jos käytät ICMP-paketteja.
- Traceroute voi antaa arvokasta tietoa verkon ongelmista, joten analysoi tuloksia huolellisesti.