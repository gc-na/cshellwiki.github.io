# [Nederlandse] C Shell (csh) minikube gebruik: Beheer lokale Kubernetes-clusters

## Overzicht
De `minikube`-opdracht is een hulpmiddel waarmee gebruikers eenvoudig een lokale Kubernetes-cluster kunnen opzetten en beheren. Het is ideaal voor ontwikkelaars die Kubernetes willen leren of applicaties willen testen in een gecontroleerde omgeving.

## Gebruik
De basis syntaxis van de `minikube`-opdracht is als volgt:

```csh
minikube [opties] [argumenten]
```

## Veelvoorkomende opties
- `start`: Start een nieuwe minikube-cluster.
- `stop`: Stop de actieve minikube-cluster.
- `delete`: Verwijder de minikube-cluster.
- `status`: Toon de status van de minikube-cluster.
- `dashboard`: Open het Kubernetes-dashboard in de webbrowser.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `minikube`-opdracht:

### Start een nieuwe cluster
```csh
minikube start
```

### Stop de actieve cluster
```csh
minikube stop
```

### Verwijder de cluster
```csh
minikube delete
```

### Controleer de status van de cluster
```csh
minikube status
```

### Open het Kubernetes-dashboard
```csh
minikube dashboard
```

## Tips
- Zorg ervoor dat je de juiste virtualisatie-instellingen hebt geconfigureerd voordat je `minikube` start.
- Gebruik de `--driver` optie om een specifieke virtualisatie-driver te kiezen, zoals `virtualbox` of `docker`.
- Controleer regelmatig de status van je cluster om ervoor te zorgen dat alles soepel verloopt.