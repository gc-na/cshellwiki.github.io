# [Linux] Bash diff käyttö: vertaa tiedostoja

## Overview
`diff`-komento on työkalu, joka vertaa kahta tiedostoa ja näyttää niiden väliset erot. Se on erityisen hyödyllinen ohjelmoijille ja järjestelmänvalvojille, jotka tarvitsevat tietoa tiedostojen muutoksista.

## Usage
Perussyntaksi `diff`-komennolle on seuraava:

```bash
diff [options] [arguments]
```

## Common Options
- `-u`: Näyttää erot "unified" muodossa, mikä tekee eroista helpommin luettavia.
- `-c`: Näyttää erot "context" muodossa, joka antaa enemmän kontekstia muutoksista.
- `-i`: Ignoroi isot ja pienet kirjaimet vertailussa.
- `-w`: Ignoroi tyhjät merkit (välilyönnit) vertailussa.

## Common Examples
### Perusvertailu
Vertaa kahta tiedostoa ja näyttää niiden erot.
```bash
diff file1.txt file2.txt
```

### Unified-muoto
Näyttää erot unified-muodossa.
```bash
diff -u file1.txt file2.txt
```

### Context-muoto
Näyttää erot context-muodossa.
```bash
diff -c file1.txt file2.txt
```

### Isot ja pienet kirjaimet huomioimatta
Vertaa tiedostoja ilman kirjainten erottelua.
```bash
diff -i file1.txt file2.txt
```

## Tips
- Käytä `-u`-vaihtoehtoa, kun haluat luettavampia eroja, erityisesti kun jaat muutoksia tiimisi kanssa.
- Voit ohjata `diff`-komennon tulosteen tiedostoon käyttämällä `>`-merkkiä, mikä helpottaa erojen tallentamista.
- Hyödynnä `diff`-komentoa versionhallintajärjestelmissä, kuten Git, saadaksesi selkeämmän käsityksen tiedostomuutoksista.