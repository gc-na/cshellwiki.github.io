# [Linux] Bash mount käyttö: Liittää tiedostojärjestelmiä

## Yleiskatsaus
`mount`-komento on käytössä Linux- ja Unix-pohjaisissa käyttöjärjestelmissä, ja sen avulla voidaan liittää tiedostojärjestelmiä, kuten kiintolevyjä tai USB-muistitikkuja, järjestelmän tiedostohierarkiaan. Tämä mahdollistaa tiedostojen ja kansioiden käytön liitetyistä laitteista.

## Käyttö
Perussyntaksi `mount`-komennolle on seuraava:

```bash
mount [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-t tyyppi`: Määrittää liitettävän tiedostojärjestelmän tyypin (esim. ext4, ntfs).
- `-o vaihtoehdot`: Määrittää liittämiseen liittyviä vaihtoehtoja, kuten `ro` (vain luku) tai `rw` (luku ja kirjoitus).
- `-a`: Liittää kaikki tiedostojärjestelmät, jotka on määritelty `/etc/fstab`-tiedostossa.
- `-r`: Liittää tiedostojärjestelmän vain luku -tilassa.

## Yleiset esimerkit
### 1. Liitä USB-muistitikku
```bash
mount /dev/sdb1 /media/usb
```
Tässä komennossa `/dev/sdb1` on USB-muistitikun laitepolku ja `/media/usb` on kansio, johon se liitetään.

### 2. Liitä NTFS-tiedostojärjestelmä
```bash
mount -t ntfs-3g /dev/sdc1 /mnt/ntfsdrive
```
Tässä esimerkissä liitetään NTFS-tiedostojärjestelmä `/dev/sdc1`-laitteesta `/mnt/ntfsdrive`-kansioon.

### 3. Liitä tiedostojärjestelmä vain luku -tilassa
```bash
mount -o ro /dev/sda1 /mnt/read_only
```
Tässä komennossa liitetään `/dev/sda1` vain luku -tilassa `/mnt/read_only`-kansioon.

### 4. Liitä kaikki tiedostojärjestelmät
```bash
mount -a
```
Tämä komento liittää kaikki tiedostojärjestelmät, jotka on määritelty `/etc/fstab`-tiedostossa.

## Vinkit
- Varmista, että liitettävä kansio on olemassa ennen `mount`-komennon suorittamista.
- Käytä `umount`-komentoa irrottaaksesi liitetyn tiedostojärjestelmän turvallisesti.
- Tarkista liitetyt tiedostojärjestelmät komennolla `df -h` tai `mount` ilman argumentteja.