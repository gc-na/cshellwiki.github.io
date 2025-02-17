# [Linux] Bash helm användning: Hantera Kubernetes-applikationer

## Översikt
Helm är en pakethanterare för Kubernetes som gör det enklare att installera, uppgradera och hantera applikationer i en Kubernetes-miljö. Genom att använda Helm kan du definiera, installera och uppgradera applikationer med hjälp av "charts", vilket är samlingar av resurser som beskriver en applikation.

## Användning
Den grundläggande syntaxen för helm-kommandot är:

```bash
helm [alternativ] [argument]
```

## Vanliga alternativ
- `install`: Installerar en ny release av en chart.
- `upgrade`: Uppgraderar en befintlig release med en ny version av en chart.
- `uninstall`: Avinstallerar en release.
- `list`: Visar en lista över installerade releases.
- `repo`: Hanterar Helm-repositories.

## Vanliga exempel
Här är några praktiska exempel på hur du använder helm:

### Installera en chart
För att installera en chart, använd följande kommando:

```bash
helm install my-release my-chart
```

### Uppgradera en release
För att uppgradera en befintlig release:

```bash
helm upgrade my-release my-chart
```

### Avinstallera en release
För att avinstallera en release:

```bash
helm uninstall my-release
```

### Lista installerade releases
För att se en lista över installerade releases:

```bash
helm list
```

### Hantera repositories
För att lägga till ett nytt repository:

```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- Se till att alltid använda den senaste versionen av Helm för att få tillgång till de senaste funktionerna och säkerhetsuppdateringarna.
- Använd `helm search` för att snabbt hitta charts i dina registrerade repositories.
- Skapa egna charts för att standardisera installationen av dina applikationer och underlätta hanteringen.