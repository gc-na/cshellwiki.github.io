# [Linux] Bash helm brug: Administrer Kubernetes applikationer

## Oversigt
Helm er en pakkehåndtering til Kubernetes, der gør det nemt at installere, opgradere og administrere applikationer i et Kubernetes-miljø. Det fungerer ved at bruge "charts", som er samlinger af filer, der beskriver en Kubernetes-applikation.

## Brug
Den grundlæggende syntaks for helm-kommandoen er:

```bash
helm [options] [arguments]
```

## Almindelige muligheder
- `install`: Installerer en ny chart.
- `upgrade`: Opgraderer en eksisterende release.
- `uninstall`: Afinstallerer en release.
- `list`: Viser en liste over installerede releases.
- `repo`: Håndterer Helm repositories.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger helm:

### Installere en chart
For at installere en chart, kan du bruge følgende kommando:

```bash
helm install my-release my-chart
```

### Opgradere en release
For at opgradere en eksisterende release, kan du bruge:

```bash
helm upgrade my-release my-chart
```

### Afinstallere en release
For at afinstallere en release, kan du køre:

```bash
helm uninstall my-release
```

### Liste over installerede releases
For at se alle installerede releases, kan du bruge:

```bash
helm list
```

### Tilføje et repository
For at tilføje et Helm repository, kan du bruge:

```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- Sørg for at opdatere dit repository med `helm repo update` for at få de nyeste charts.
- Brug `--dry-run` flaget til at simulere installationen, før du udfører den, så du kan se, hvad der vil ske.
- Hold dine charts organiseret og dokumenteret for nem vedligeholdelse og opgraderinger.