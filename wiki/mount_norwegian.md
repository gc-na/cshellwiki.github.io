# [Linux] Bash mount bruk: Monter filsystemer

## Oversikt
`mount`-kommandoen brukes til å montere filsystemer i Linux. Dette gjør det mulig for brukeren å få tilgang til filer og kataloger på enheten som er tilkoblet systemet, som for eksempel en harddisk, USB-minnepinne eller nettverkslag.

## Bruk
Den grunnleggende syntaksen for `mount`-kommandoen er som følger:

```
mount [alternativer] [enhet] [monteringspunkt]
```

## Vanlige alternativer
- `-t` : Angir typen filsystem (for eksempel ext4, ntfs, etc.).
- `-o` : Spesifiserer monteringsalternativer (som read-only, noexec, etc.).
- `-a` : Monterer alle filsystemer som er oppført i `/etc/fstab`.
- `-r` : Monterer filsystemet som skrivebeskyttet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mount`-kommandoen:

### Montere en USB-enhet
For å montere en USB-enhet som er tilkoblet systemet, kan du bruke følgende kommando:

```bash
mount /dev/sdb1 /mnt/usb
```

### Montere et nettverksfilsystem
For å montere et nettverksfilsystem (NFS), kan du bruke:

```bash
mount -t nfs 192.168.1.100:/export /mnt/nfs
```

### Monter alle filsystemer fra fstab
For å montere alle filsystemer som er oppført i `/etc/fstab`, kan du bruke:

```bash
mount -a
```

### Monter som skrivebeskyttet
For å montere et filsystem som skrivebeskyttet, kan du bruke:

```bash
mount -o ro /dev/sdc1 /mnt/readonly
```

## Tips
- Sørg for at monteringspunktet eksisterer før du prøver å montere en enhet.
- Bruk `df -h` for å sjekke hvilke filsystemer som er montert og hvor mye plass som er tilgjengelig.
- Husk å bruke `umount` for å demontere filsystemet før du fjerner enheten for å unngå datatap.