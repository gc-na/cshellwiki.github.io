# [Linux] Bash systemctl bruk: Administrere systemtjenester

## Oversikt
`systemctl` er et kommandolinjeverktøy som brukes til å kontrollere systemd-system- og tjenestestyring. Det lar brukere starte, stoppe, aktivere, deaktivere og overvåke tjenester og systemprosedyrer.

## Bruk
Grunnleggende syntaks for `systemctl`-kommandoen er som følger:

```bash
systemctl [alternativer] [argumenter]
```

## Vanlige alternativer
- `start`: Starter en tjeneste.
- `stop`: Stopper en aktiv tjeneste.
- `restart`: Starter en tjeneste på nytt.
- `status`: Viser statusen til en tjeneste.
- `enable`: Aktiverer en tjeneste ved oppstart.
- `disable`: Deaktiverer en tjeneste ved oppstart.
- `list-units`: Viser en liste over aktive enheter.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `systemctl`:

- For å starte en tjeneste:
  ```bash
  systemctl start httpd
  ```

- For å stoppe en tjeneste:
  ```bash
  systemctl stop httpd
  ```

- For å sjekke statusen til en tjeneste:
  ```bash
  systemctl status httpd
  ```

- For å aktivere en tjeneste ved oppstart:
  ```bash
  systemctl enable httpd
  ```

- For å deaktivere en tjeneste ved oppstart:
  ```bash
  systemctl disable httpd
  ```

- For å liste alle aktive enheter:
  ```bash
  systemctl list-units --type=service
  ```

## Tips
- Bruk `systemctl status [tjeneste]` for å få detaljert informasjon om en tjeneste, inkludert loggutdata.
- Vær oppmerksom på at du kanskje trenger root-rettigheter for å utføre visse handlinger med `systemctl`. Bruk `sudo` hvis nødvendig.
- For å se alle tilgjengelige alternativer og kommandoer, kan du bruke `systemctl --help`.