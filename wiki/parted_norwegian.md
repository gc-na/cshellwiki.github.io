# [Linux] Bash parted bruk: Administrere partisjoner på disk

## Oversikt
`parted` er et kommandolinjeverktøy som brukes til å administrere partisjoner på lagringsenheter. Det gir brukerne mulighet til å opprette, slette, endre størrelse på og formatere partisjoner, samt vise informasjon om eksisterende partisjoner.

## Bruk
Grunnleggende syntaks for `parted`-kommandoen er som følger:

```bash
parted [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l` : Viser en liste over tilgjengelige lagringsenheter og deres partisjoner.
- `mkpart` : Oppretter en ny partisjon.
- `rm` : Sletter en eksisterende partisjon.
- `resizepart` : Endrer størrelsen på en eksisterende partisjon.
- `print` : Viser informasjon om partisjonene på den valgte enheten.

## Vanlige eksempler

### Liste over partisjoner
For å vise alle partisjoner på systemet, kan du bruke:

```bash
parted -l
```

### Opprette en ny partisjon
For å opprette en ny partisjon fra 1GB til 5GB på en enhet (for eksempel `/dev/sda`):

```bash
parted /dev/sda mkpart primary ext4 1GB 5GB
```

### Slette en partisjon
For å slette partisjon nummer 2 på en enhet:

```bash
parted /dev/sda rm 2
```

### Endre størrelse på en partisjon
For å endre størrelsen på partisjon nummer 1 til 10GB:

```bash
parted /dev/sda resizepart 1 10GB
```

### Vise partisjonsinformasjon
For å vise detaljer om partisjonene på en spesifikk enhet:

```bash
parted /dev/sda print
```

## Tips
- Sørg for å ta sikkerhetskopi av viktige data før du gjør endringer på partisjoner.
- Bruk `parted` med forsiktighet, da feil kommandoer kan føre til datatap.
- Kjør `parted` med superbrukerrettigheter (bruk `sudo`) for å få tilgang til alle funksjoner.