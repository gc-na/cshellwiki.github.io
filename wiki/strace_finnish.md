# [Linux] Bash strace käyttö: Ohjelmien järjestelmäkutsujen jäljittäminen

## Yleiskatsaus
`strace` on työkalu, joka mahdollistaa ohjelmien järjestelmäkutsujen ja signaalien jäljittämisen. Se on erityisen hyödyllinen virheiden etsinnässä ja ohjelmien toiminnan analysoinnissa, sillä se näyttää, mitä järjestelmäkutsuja ohjelma tekee ja miten se vuorovaikuttaa käyttöjärjestelmän kanssa.

## Käyttö
Perussyntaksi `strace`-komennolle on seuraava:

```bash
strace [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-o tiedosto`: Tallentaa jäljityksen tulokset määritettyyn tiedostoon.
- `-e ilmiö`: Suodattaa jäljitettävät järjestelmäkutsut tiettyyn ilmiöön, kuten `open`, `read` tai `write`.
- `-p prosessi_id`: Jäljittää jo käynnissä olevaa prosessia, jonka ID on määritetty.
- `-c`: Näyttää tilastotiedot järjestelmäkutsujen käytöstä sen sijaan, että tulostaisi jokaisen kutsun erikseen.

## Yleiset esimerkit
1. **Perus jäljitys**:
   Jäljitä ohjelman `ls` järjestelmäkutsut.
   ```bash
   strace ls
   ```

2. **Tulosten tallentaminen tiedostoon**:
   Jäljitä ohjelman `cat` järjestelmäkutsut ja tallenna tulokset tiedostoon `output.txt`.
   ```bash
   strace -o output.txt cat myfile.txt
   ```

3. **Tietyt järjestelmäkutsut**:
   Jäljitä vain `open`- ja `read`-kutsuja ohjelmasta `grep`.
   ```bash
   strace -e trace=open,read grep "text" myfile.txt
   ```

4. **Jo käynnissä olevan prosessin jäljittäminen**:
   Jäljitä prosessia, jonka ID on 1234.
   ```bash
   strace -p 1234
   ```

5. **Tilastojen näyttäminen**:
   Näytä tilastotiedot järjestelmäkutsujen käytöstä ohjelmasta `find`.
   ```bash
   strace -c find /home
   ```

## Vinkit
- Käytä `-o`-vaihtoehtoa, jos haluat tallentaa tulokset ja analysoida niitä myöhemmin.
- Suodata järjestelmäkutsuja `-e`-vaihtoehdolla, jotta saat tarkempaa tietoa ongelmista.
- Muista, että `strace` voi hidastaa ohjelman suoritusta, joten käytä sitä vain tarpeen mukaan.
- Hyödynnä `-c`-vaihtoehtoa saadaksesi nopean yleiskatsauksen ohjelman suorituskyvystä.