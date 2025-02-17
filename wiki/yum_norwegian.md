# [Linux] Bash yum bruk: Administrere pakker på systemet

## Oversikt
`yum` (Yellowdog Updater Modified) er et kommandolinjeverktøy for pakkehåndtering på Linux-systemer, spesielt for distribusjoner som Red Hat, CentOS og Fedora. Det brukes til å installere, oppdatere, fjerne og administrere programvarepakker.

## Bruk
Grunnleggende syntaks for `yum`-kommandoen er som følger:

```bash
yum [alternativer] [argumenter]
```

## Vanlige alternativer
- `install`: Installerer en eller flere pakker.
- `remove`: Fjerner en eller flere pakker.
- `update`: Oppdaterer alle installerte pakker til den nyeste versjonen.
- `search`: Søker etter pakker i depotene.
- `info`: Viser informasjon om en spesifikk pakke.
- `list`: Viser en liste over tilgjengelige eller installerte pakker.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du bruker `yum`:

### Installere en pakke
For å installere en pakke, for eksempel `httpd` (Apache webserver), kan du bruke følgende kommando:

```bash
yum install httpd
```

### Fjerne en pakke
For å fjerne en pakke, for eksempel `httpd`, kan du bruke:

```bash
yum remove httpd
```

### Oppdatere alle pakker
For å oppdatere alle installerte pakker til den nyeste versjonen, kjør:

```bash
yum update
```

### Søke etter en pakke
Hvis du vil søke etter en pakke, for eksempel `vim`, kan du bruke:

```bash
yum search vim
```

### Vise informasjon om en pakke
For å vise informasjon om en spesifikk pakke, for eksempel `vim`, kan du bruke:

```bash
yum info vim
```

## Tips
- Kjør `yum clean all` for å rydde opp i cache og frigjøre plass.
- Bruk `yum list installed` for å se en liste over alle installerte pakker.
- Vær oppmerksom på avhengigheter; `yum` håndterer dem automatisk, men det er lurt å være klar over hvilke pakker som blir installert eller fjernet.