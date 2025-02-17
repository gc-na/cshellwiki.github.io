# [Linux] Bash helm bruk: Administrere Kubernetes-applikasjoner

## Oversikt
Helm er en pakkehåndterer for Kubernetes som gjør det enklere å installere og administrere applikasjoner i Kubernetes-klynger. Den lar brukere definere, installere og oppgradere komplekse applikasjoner ved hjelp av "charts", som er samlinger av Kubernetes-manifester.

## Bruk
Den grunnleggende syntaksen for helm-kommandoen er som følger:

```bash
helm [alternativer] [argumenter]
```

## Vanlige alternativer
- `install`: Installerer en ny chart i Kubernetes-klyngen.
- `upgrade`: Oppgraderer en eksisterende chart til en ny versjon.
- `uninstall`: Fjerner en installert chart fra klyngen.
- `list`: Viser en liste over installerte charts.
- `repo`: Administrerer Helm-repositorier.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du bruker helm-kommandoen:

### Installere en chart
For å installere en chart, kan du bruke følgende kommando:

```bash
helm install my-release stable/mysql
```

### Oppgradere en chart
For å oppgradere en eksisterende chart, kan du bruke:

```bash
helm upgrade my-release stable/mysql
```

### Avinstallere en chart
For å avinstallere en chart, kan du bruke:

```bash
helm uninstall my-release
```

### Liste over installerte charts
For å se en liste over alle installerte charts, kan du bruke:

```bash
helm list
```

### Legge til et nytt repository
For å legge til et nytt Helm-repository, kan du bruke:

```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- Sørg for å oppdatere Helm-repositoriene dine regelmessig med `helm repo update` for å få de nyeste chartene.
- Bruk `--dry-run` alternativet for å simulere installasjoner eller oppgraderinger før du utfører dem, slik at du kan se hva som vil skje.
- Organiser chartene dine i egne kataloger for bedre oversikt og administrasjon.