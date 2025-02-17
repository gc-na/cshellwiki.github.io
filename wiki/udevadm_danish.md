# [Linux] Bash udevadm brug: Administrer enhedsdrev

## Oversigt
`udevadm` er et kommandolinjeværktøj, der bruges til at interagere med udev, som er en enhedshåndteringsdæmon i Linux. Det giver mulighed for at overvåge, administrere og ændre enhedsoplysninger i realtid.

## Brug
Den grundlæggende syntaks for `udevadm` er:

```bash
udevadm [muligheder] [argumenter]
```

## Almindelige muligheder
- `info`: Viser oplysninger om enheden.
- `trigger`: Udløser udev-handlinger for enheder.
- `settle`: Venter på, at udev-handlinger er afsluttet.
- `monitor`: Overvåger udev-begivenheder i realtid.
- `control`: Kontrollerer udev-dæmonens tilstand.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `udevadm` kan bruges:

### Vis oplysninger om en enhed
For at få oplysninger om en specifik enhed kan du bruge:

```bash
udevadm info --query=all --name=/dev/sda
```

### Udløs udev-handlinger
For at udløse udev-handlinger for alle enheder kan du køre:

```bash
udevadm trigger
```

### Vent på, at udev-handlinger er afsluttet
For at vente på, at alle udev-handlinger er afsluttet, kan du bruge:

```bash
udevadm settle
```

### Overvåg udev-begivenheder
For at overvåge udev-begivenheder i realtid, kan du køre:

```bash
udevadm monitor
```

### Kontroller udev-dæmonens tilstand
For at kontrollere tilstanden af udev-dæmonen, kan du bruge:

```bash
udevadm control --reload-rules
```

## Tips
- Brug `udevadm monitor` til at fejlsøge enhedsproblemer ved at se, hvilke begivenheder der genereres.
- Når du ændrer regler, skal du altid køre `udevadm control --reload-rules` for at sikre, at ændringerne træder i kraft.
- Vær opmærksom på, at nogle `udevadm`-kommandoer kræver root-rettigheder, så du skal muligvis bruge `sudo`.