# [Linux] Bash lvm bruk: Håndtering av logiske volum

## Oversikt
`lvm` (Logical Volume Manager) er et verktøy for administrasjon av logiske volum i Linux. Det gir fleksibilitet til å opprette, endre og slette volumgrupper og logiske volum, noe som gjør det enklere å håndtere lagringsressurser.

## Bruk
Grunnleggende syntaks for `lvm`-kommandoen er:

```
lvm [alternativer] [argumenter]
```

## Vanlige alternativer
- `vgcreate`: Oppretter en ny volumgruppe.
- `lvcreate`: Oppretter et nytt logisk volum.
- `lvremove`: Fjerner et logisk volum.
- `vgextend`: Utvider en eksisterende volumgruppe.
- `lvextend`: Utvider et logisk volum.

## Vanlige eksempler

### Opprette en volumgruppe
For å opprette en volumgruppe kalt `vg1` med fysisk volum `/dev/sda1`, kan du bruke følgende kommando:

```bash
lvm vgcreate vg1 /dev/sda1
```

### Opprette et logisk volum
For å opprette et logisk volum kalt `lv1` på volumgruppen `vg1` med størrelse 10 GB, bruker du:

```bash
lvm lvcreate -n lv1 -L 10G vg1
```

### Utvide et logisk volum
For å utvide det logiske volumet `lv1` med 5 GB, kan du bruke:

```bash
lvm lvextend -L +5G /dev/vg1/lv1
```

### Fjerne et logisk volum
For å fjerne det logiske volumet `lv1`, bruker du:

```bash
lvm lvremove /dev/vg1/lv1
```

## Tips
- Sørg for å ta sikkerhetskopi av viktige data før du utfører operasjoner som kan endre eller slette volum.
- Bruk `lvm`-kommandoen med `--help` for å få en liste over tilgjengelige alternativer og deres beskrivelse.
- Vær oppmerksom på at endringer i volum kan kreve at filsystemet blir montert på nytt for å gjenspeile endringene.