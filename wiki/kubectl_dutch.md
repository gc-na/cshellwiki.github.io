# [Linux] C Shell (csh) kubectl gebruik: Beheer Kubernetes-clusters

## Overzicht
De `kubectl`-opdracht is een krachtige tool die wordt gebruikt voor het beheren van Kubernetes-clusters. Met `kubectl` kunnen gebruikers verschillende acties uitvoeren, zoals het implementeren van applicaties, het inspecteren van clusterstatussen en het beheren van resources binnen een Kubernetes-omgeving.

## Gebruik
De basis syntaxis van de `kubectl`-opdracht is als volgt:

```bash
kubectl [opties] [argumenten]
```

## Veelvoorkomende opties
- `-n, --namespace`: Specificeert de namespace waarin de opdracht moet worden uitgevoerd.
- `-o, --output`: Bepaalt het outputformaat, zoals `json`, `yaml`, of `wide`.
- `--kubeconfig`: Geeft het pad op naar het kubeconfig-bestand dat moet worden gebruikt.
- `--context`: Specificeert de context die moet worden gebruikt voor de opdracht.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `kubectl`:

### Lijst van alle pods
```bash
kubectl get pods
```

### Lijst van services in een specifieke namespace
```bash
kubectl get services -n mijn-namespace
```

### Toepassing implementeren vanuit een YAML-bestand
```bash
kubectl apply -f mijn-applicatie.yaml
```

### Informatie over een specifieke pod
```bash
kubectl describe pod mijn-pod
```

### Logs van een specifieke pod bekijken
```bash
kubectl logs mijn-pod
```

## Tips
- Gebruik de `--dry-run` optie om te zien wat er zou gebeuren zonder daadwerkelijk wijzigingen aan te brengen.
- Maak gebruik van `kubectl explain` om meer te leren over de verschillende resources en hun velden.
- Houd je kubeconfig-bestand georganiseerd door contexten en namespaces goed te beheren, vooral bij het werken met meerdere clusters.