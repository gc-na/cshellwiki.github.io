# [Linux] Bash tcpdump käyttö: Veroliikenteen kaappaus ja analysointi

## Yleiskatsaus
Tcpdump on tehokas komentorivipohjainen työkalu, jota käytetään verkkoliikenteen kaappaamiseen ja analysoimiseen. Se mahdollistaa pakettien tarkastelun reaaliajassa ja on erityisen hyödyllinen verkko-ongelmien vianetsinnässä sekä turvallisuustarkastuksissa.

## Käyttö
Perussyntaksi tcpdump-komennolle on seuraava:

```bash
tcpdump [options] [arguments]
```

## Yleiset vaihtoehdot
- `-i <interface>`: Määrittää verkkoliittymän, jolta liikennettä kaapataan.
- `-n`: Estää DNS-nimien kääntämisen, mikä nopeuttaa tulosten näyttämistä.
- `-c <count>`: Määrittää, kuinka monta pakettia tcpdump kaappaa ennen lopettamista.
- `-w <file>`: Tallentaa kaapatut paketit tiedostoon.
- `-r <file>`: Lukee kaapatut paketit tiedostosta.

## Yleiset esimerkit
### 1. Verkkoliikenteen kaappaaminen tietyltä liittymältä
```bash
tcpdump -i eth0
```
Tämä komento kaappaa kaiken liikenteen `eth0`-liittymältä.

### 2. Kaappaa vain tietyt paketit
```bash
tcpdump -i eth0 port 80
```
Tämä komento kaappaa vain HTTP-liikenteen (portti 80) `eth0`-liittymältä.

### 3. Kaappaa rajoitettu määrä paketteja
```bash
tcpdump -i eth0 -c 10
```
Tässä komennossa tcpdump kaappaa vain 10 pakettia ja lopettaa sitten.

### 4. Tallenna kaapatut paketit tiedostoon
```bash
tcpdump -i eth0 -w liikenne.pcap
```
Tämä komento tallentaa kaapatut paketit `liikenne.pcap`-tiedostoon analysoitavaksi myöhemmin.

### 5. Lue kaapattu liikenne tiedostosta
```bash
tcpdump -r liikenne.pcap
```
Tämä komento lukee ja näyttää aiemmin tallennetut paketit `liikenne.pcap`-tiedostosta.

## Vinkit
- Käytä `-n`-vaihtoehtoa, jos et tarvitse DNS-nimiä, jotta tulokset tulevat nopeammin näkyviin.
- Varmista, että sinulla on tarvittavat oikeudet verkkoliikenteen kaappaamiseen (esim. suorita komento root-oikeuksilla).
- Käytä suodattimia (kuten `port`, `host`, `src`, `dst`) tarkentaaksesi kaappausta vain niihin paketteihin, jotka ovat sinulle relevantteja.
- Tallenna kaapatut paketit tiedostoon analysoitavaksi myöhemmin, erityisesti jos liikenne on suurta.