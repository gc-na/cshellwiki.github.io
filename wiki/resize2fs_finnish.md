# [Linux] Bash resize2fs käyttö: Tiedostojärjestelmän koon muuttaminen

## Yleiskatsaus
`resize2fs` on komento, jota käytetään tiedostojärjestelmän koon muuttamiseen Linux-järjestelmissä. Se mahdollistaa tiedostojärjestelmän laajentamisen tai pienentämisen, mikä on hyödyllistä, kun halutaan optimoida levytilan käyttöä.

## Käyttö
Perussyntaksi `resize2fs`-komennolle on seuraava:

```bash
resize2fs [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-f`: Pakottaa tiedostojärjestelmän koon muuttamisen, vaikka se ei olisi suositeltavaa.
- `-p`: Näyttää edistymispalkin koon muuttamisen aikana.
- `-s`: Pienentää tiedostojärjestelmää vain, jos se on mahdollista.
- `-M`: Pienentää tiedostojärjestelmää mahdollisimman pieneksi.

## Yleiset esimerkit
### Tiedostojärjestelmän laajentaminen
Laajenna tiedostojärjestelmää, joka on liitetty `/dev/sda1`:

```bash
resize2fs /dev/sda1
```

### Tiedostojärjestelmän pienentäminen
Pienennä tiedostojärjestelmää, joka on liitetty `/dev/sda1`, esimerkiksi 20 GB:ksi:

```bash
resize2fs -s /dev/sda1 20G
```

### Edistymispalkin näyttäminen
Näytä edistymispalkki tiedostojärjestelmän koon muuttamisen aikana:

```bash
resize2fs -p /dev/sda1
```

## Vinkit
- Varmista, että tiedostojärjestelmä on irrotettu tai että se on vain luku -tilassa ennen sen pienentämistä.
- Ota varmuuskopio tärkeistä tiedoista ennen tiedostojärjestelmän koon muuttamista.
- Tarkista tiedostojärjestelmän eheys `e2fsck`-komennolla ennen koon muuttamista.