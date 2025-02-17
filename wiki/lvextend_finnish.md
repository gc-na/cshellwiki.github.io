# [Linux] Bash lvextend käyttö: Laajentaa loogista volyymia

## Yleiskatsaus
`lvextend`-komento on käytössä Linux-järjestelmissä loogisten volyymien laajentamiseen. Se mahdollistaa tallennustilan lisäämisen olemassa oleviin loogisiin volyymeihin, mikä on erityisen hyödyllistä, kun tilaa tarvitaan lisää ilman, että tiedostojärjestelmää tarvitsee luoda uudelleen.

## Käyttö
Perussyntaksi `lvextend`-komennolle on seuraava:

```bash
lvextend [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-L, --size`: Määrittää uuden koon loogiselle volyymille.
- `-l, --extents`: Määrittää laajennettavien laajennusten määrän.
- `-r, --resizefs`: Laajentaa tiedostojärjestelmää automaattisesti loogisen volyymin laajentamisen jälkeen.

## Yleiset esimerkit
1. Laajenna loogista volyymia tiettyyn kokoon:
   ```bash
   lvextend -L +10G /dev/vg1/lv1
   ```

2. Laajenna loogista volyymia tietyllä määrällä laajennuksia:
   ```bash
   lvextend -l +100 /dev/vg1/lv1
   ```

3. Laajenna loogista volyymia ja tiedostojärjestelmää samanaikaisesti:
   ```bash
   lvextend -L +5G -r /dev/vg1/lv1
   ```

## Vinkit
- Varmista, että sinulla on riittävästi tilaa fyysisissä volyymeissä ennen laajentamista.
- Käytä `-r`-vaihtoehtoa, jos haluat automaattisesti laajentaa tiedostojärjestelmää, mikä säästää aikaa ja vaivannäköä.
- Tarkista loogisten volyymien ja fyysisten volyymien tila ennen ja jälkeen laajentamisen varmistaaksesi, että kaikki sujui suunnitellusti.