# [Linux] Bash vgcreate Bruk: Oppretting av volumgrupper

## Oversikt
`vgcreate` er en Bash-kommando som brukes til å opprette en ny volumgruppe i Logical Volume Manager (LVM) på Linux-systemer. Volumgrupper lar deg samle flere fysiske volumer til en logisk enhet, noe som gjør det enklere å administrere lagringsplass.

## Bruk
Grunnleggende syntaks for `vgcreate`-kommandoen er som følger:

```bash
vgcreate [alternativer] [navn_på_volumgruppe] [fysiske_volumer]
```

## Vanlige alternativer
- `-s, --stripes <antall>`: Angir antall striper for volumgruppen.
- `-p, --max-pv <antall>`: Setter maksimum antall fysiske volumer i volumgruppen.
- `--metadatasize <størrelse>`: Angir størrelsen på metadataene for volumgruppen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `vgcreate`:

### Eksempel 1: Opprette en enkel volumgruppe
```bash
vgcreate vg_data /dev/sda1 /dev/sdb1
```
Dette oppretter en volumgruppe kalt `vg_data` som inkluderer de fysiske volumene `/dev/sda1` og `/dev/sdb1`.

### Eksempel 2: Opprette en volumgruppe med spesifikasjoner
```bash
vgcreate -s 64k -p 5 vg_backup /dev/sdc1
```
Her oppretter vi en volumgruppe kalt `vg_backup` med striper på 64k og maksimalt 5 fysiske volumer, inkludert `/dev/sdc1`.

### Eksempel 3: Opprette en volumgruppe med metadata størrelse
```bash
vgcreate --metadatasize 256k vg_media /dev/sdd1
```
Dette oppretter en volumgruppe kalt `vg_media` med metadata størrelse på 256k, inkludert det fysiske volumet `/dev/sdd1`.

## Tips
- Sørg for at de fysiske volumene du bruker er tilgjengelige og ikke i bruk av andre systemprosesser.
- Bruk `vgdisplay` for å vise informasjon om eksisterende volumgrupper etter oppretting.
- Vær oppmerksom på at endringer i volumgrupper kan påvirke datatilgang, så det er lurt å ta sikkerhetskopier før du gjør store endringer.