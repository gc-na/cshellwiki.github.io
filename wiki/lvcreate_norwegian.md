# [Linux] Bash lvcreate Bruk: Oppretting av logiske volumer

## Oversikt
`lvcreate` er et Bash-kommando som brukes til å opprette logiske volumer i Linux Logical Volume Manager (LVM). Dette verktøyet gir deg muligheten til å administrere diskplass mer fleksibelt ved å opprette, endre og slette logiske volumer.

## Bruk
Grunnleggende syntaks for `lvcreate`-kommandoen er som følger:

```bash
lvcreate [alternativer] [argumenter]
```

## Vanlige alternativer
- `-L, --size`: Angir størrelsen på det logiske volumet.
- `-n, --name`: Setter navnet på det logiske volumet.
- `-m, --mirrors`: Angir antall speil av volumet.
- `-Z, --zero`: Angir om volumet skal nullstilles.
- `-C, --contiguous`: Oppretter et sammenhengende logisk volum.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `lvcreate`:

### Eksempel 1: Opprette et logisk volum med spesifisert størrelse
```bash
lvcreate -L 10G -n mitt_volum vg1
```
Dette oppretter et logisk volum kalt `mitt_volum` med en størrelse på 10 GB i volumgruppen `vg1`.

### Eksempel 2: Opprette et speilet logisk volum
```bash
lvcreate -L 20G -m 1 -n speilet_volum vg1
```
Her opprettes et speilet logisk volum kalt `speilet_volum` med en størrelse på 20 GB i volumgruppen `vg1`.

### Eksempel 3: Opprette et logisk volum med sammenhengende plass
```bash
lvcreate -L 5G -C y -n sammenhengende_volum vg1
```
Dette oppretter et sammenhengende logisk volum kalt `sammenhengende_volum` med en størrelse på 5 GB i volumgruppen `vg1`.

## Tips
- Sørg for at volumgruppen har tilstrekkelig ledig plass før du oppretter et logisk volum.
- Bruk `lvdisplay` for å vise informasjon om eksisterende logiske volumer.
- Vurder å bruke `--mirrors` for å øke påliteligheten til viktige volumer.
- Husk å ta sikkerhetskopi av dataene dine før du gjør endringer i volumene.