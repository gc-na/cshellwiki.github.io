# [Linux] Bash hostnamectl Bruk: Administrer vertsnavn og relaterte innstillinger

## Oversikt
`hostnamectl` er et kommandoverktøy som brukes til å administrere vertsnavn og relaterte innstillinger på Linux-systemer. Det gir brukeren mulighet til å vise og endre vertsnavn, samt konfigurere systemets identitet.

## Bruk
Grunnleggende syntaks for `hostnamectl` er som følger:

```bash
hostnamectl [alternativer] [argumenter]
```

## Vanlige alternativer
- `set-hostname`: Endrer vertsnavnet til systemet.
- `status`: Viser informasjon om systemets nåværende vertsnavn og status.
- `set-chassis`: Angir chassistypen for systemet (f.eks. "desktop", "laptop").
- `set-icon-name`: Setter ikonet som representerer systemet i grafiske miljøer.

## Vanlige eksempler
For å vise nåværende vertsnavn og status:

```bash
hostnamectl status
```

For å endre vertsnavnet til "nytt-navn":

```bash
sudo hostnamectl set-hostname nytt-navn
```

For å angi chassistypen til "laptop":

```bash
sudo hostnamectl set-chassis laptop
```

For å sette et ikonnavn:

```bash
sudo hostnamectl set-icon-name laptop
```

## Tips
- Husk å bruke `sudo` når du endrer vertsnavn eller systeminnstillinger, da disse handlingene ofte krever administrative rettigheter.
- Etter å ha endret vertsnavnet, kan det være lurt å starte systemet på nytt for at endringene skal tre i kraft fullt ut.
- Bruk `hostnamectl status` for å bekrefte at endringene er blitt anvendt riktig.