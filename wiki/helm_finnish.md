# [Linux] Bash helm käyttö: Helm-pakettien hallinta Kubernetesissa

## Overview
Helm on Kubernetesin pakettien hallintatyökalu, joka helpottaa sovellusten asentamista, hallintaa ja päivittämistä. Se käyttää "chart"-konseptia, joka on kokoelma resursseja, joita tarvitaan sovelluksen käyttöönottoon Kubernetes-ympäristössä.

## Usage
Perussyntaksi helm-komennolle on seuraava:
```bash
helm [options] [arguments]
```

## Common Options
- `install`: Asentaa uuden chartin.
- `upgrade`: Päivittää olemassa olevan chartin.
- `uninstall`: Poistaa chartin.
- `list`: Näyttää asennetut chartit.
- `repo`: Hallitsee helm-repoja, kuten lisäämistä ja poistamista.

## Common Examples
Asennetaan uusi chart:
```bash
helm install my-release my-chart
```

Päivitetään olemassa oleva chart:
```bash
helm upgrade my-release my-chart
```

Poistetaan chart:
```bash
helm uninstall my-release
```

Näytetään asennetut chartit:
```bash
helm list
```

Lisätään uusi helm-repo:
```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- Käytä `--dry-run`-optiota ennen asennusta tai päivitystä testataksesi, mitä tapahtuu ilman todellista muutosta.
- Pidä helm-repot ajan tasalla komennolla `helm repo update`, jotta saat uusimmat chart-versiot.
- Hyödynnä helm-chartin `values.yaml`-tiedostoa mukauttaaksesi asennuksia helposti.