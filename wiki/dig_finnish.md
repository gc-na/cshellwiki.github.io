# [Linux] Bash dig käyttö: DNS-kyselyjen tekeminen

## Yleiskatsaus
`dig` (Domain Information Groper) on komento, jota käytetään DNS (Domain Name System) -kyselyjen tekemiseen. Se auttaa käyttäjiä saamaan tietoa verkkotunnuksista, IP-osoitteista ja muista DNS-tietueista.

## Käyttö
Perussyntaksi `dig`-komennolle on seuraava:
```bash
dig [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `@server`: Määrittää DNS-palvelimen, jota käytetään kyselyyn.
- `-t type`: Määrittää kyselyn tyypin (esim. A, AAAA, MX).
- `+short`: Näyttää tulokset lyhyessä muodossa.
- `+trace`: Seuraa kyselyä DNS-hierarkiassa.

## Yleiset esimerkit
1. **Peruskysely verkkotunnuksesta**:
   ```bash
   dig example.com
   ```

2. **Kysely A-tietueesta**:
   ```bash
   dig example.com A
   ```

3. **Kysely MX-tietueesta**:
   ```bash
   dig example.com MX
   ```

4. **Kysely tietyltä DNS-palvelimelta**:
   ```bash
   dig @8.8.8.8 example.com
   ```

5. **Tulosten näyttäminen lyhyessä muodossa**:
   ```bash
   dig +short example.com
   ```

6. **Kyselyn jäljittäminen**:
   ```bash
   dig +trace example.com
   ```

## Vinkit
- Käytä `+short`-vaihtoehtoa, kun haluat nopeita ja yksinkertaisia tuloksia.
- Hyödynnä `@server`-vaihtoehtoa, jos haluat testata eri DNS-palvelimia.
- Kokeile `+trace`-vaihtoehtoa, kun haluat ymmärtää, miten DNS-kyselyt kulkevat eri palvelimien läpi.