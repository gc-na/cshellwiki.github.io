# [Linux] Bash yum brug: Administrer pakker på Linux

## Oversigt
`yum` (Yellowdog Updater Modified) er en pakkehåndteringskommando, der bruges på RPM-baserede Linux-distributioner til at installere, opdatere, fjerne og administrere softwarepakker.

## Brug
Den grundlæggende syntaks for `yum`-kommandoen er:

```bash
yum [options] [arguments]
```

## Almindelige muligheder
- `install`: Installerer en eller flere pakker.
- `remove`: Fjerner en eller flere pakker.
- `update`: Opdaterer alle installerede pakker til den nyeste version.
- `search`: Søger efter pakker i repositories.
- `info`: Viser information om en specifik pakke.
- `list`: Viser en liste over tilgængelige eller installerede pakker.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `yum` kan bruges:

### Installere en pakke
For at installere en pakke, f.eks. `httpd` (Apache webserver):

```bash
yum install httpd
```

### Fjerne en pakke
For at fjerne en pakke, f.eks. `httpd`:

```bash
yum remove httpd
```

### Opdatere alle pakker
For at opdatere alle installerede pakker til den nyeste version:

```bash
yum update
```

### Søge efter en pakke
For at søge efter en pakke, f.eks. `vim`:

```bash
yum search vim
```

### Vise information om en pakke
For at vise information om en pakke, f.eks. `httpd`:

```bash
yum info httpd
```

## Tips
- Kør `yum clean all` for at rydde op i cache og frigøre plads.
- Brug `yum list installed` for at se en liste over alle installerede pakker.
- Overvej at bruge `yum groupinstall` for at installere et helt sæt af relaterede pakker på én gang.