# [Linux] Bash udevadm Bruk: Administrere enheter i Linux

## Oversikt
`udevadm` er et kommandolinjeverktøy som brukes til å administrere og kontrollere udev-systemet i Linux. Udev er ansvarlig for dynamisk håndtering av enheter i systemet, og `udevadm` gir mulighet for å overvåke, administrere og feilsøke enheter.

## Bruk
Den grunnleggende syntaksen for `udevadm` er som følger:

```bash
udevadm [alternativer] [argumenter]
```

## Vanlige alternativer
- `info`: Viser informasjon om en spesifikk enhet.
- `trigger`: Utløser udev-hendelser for enheter.
- `settle`: Venter til alle udev-hendelser er behandlet.
- `monitor`: Overvåker udev-hendelser i sanntid.
- `control`: Kontrollerer udev-demonens oppførsel.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `udevadm` kan brukes:

### 1. Vise informasjon om en enhet
For å vise informasjon om en spesifikk enhet, kan du bruke:

```bash
udevadm info --query=all --name=/dev/sda
```

### 2. Utløse udev-hendelser
Hvis du vil utløse udev-hendelser for alle enheter, kan du bruke:

```bash
udevadm trigger
```

### 3. Vente på at alle udev-hendelser skal behandles
For å vente til alle udev-hendelser er behandlet, kan du bruke:

```bash
udevadm settle
```

### 4. Overvåke udev-hendelser
For å overvåke udev-hendelser i sanntid, kan du bruke:

```bash
udevadm monitor
```

### 5. Kontrollere udev-demonen
For å kontrollere udev-demonens oppførsel, kan du bruke:

```bash
udevadm control --reload-rules
```

## Tips
- Sørg for å kjøre `udevadm` med tilstrekkelige rettigheter, da noen kommandoer kan kreve superbrukerrettigheter.
- Bruk `udevadm monitor` for å feilsøke enheter som ikke oppdages riktig.
- Husk at endringer i udev-regler kan kreve en omstart av udev-demonen for å tre i kraft.