# [Linux] Bash helm gebruik: Beheer van Kubernetes-applicaties

## Overzicht
De `helm` commandoregeltool is een pakketbeheerder voor Kubernetes, die het eenvoudig maakt om applicaties te installeren, upgraden en beheren in een Kubernetes-cluster. Helm maakt gebruik van "charts", die de configuratie en afhankelijkheden van een applicatie definiëren.

## Gebruik
De basis syntaxis van de helm-opdracht is als volgt:

```bash
helm [opties] [argumenten]
```

## Veelvoorkomende opties
- `install`: Installeert een nieuwe release van een chart.
- `upgrade`: Verhoogt een bestaande release naar een nieuwe versie van een chart.
- `uninstall`: Verwijdert een release uit het cluster.
- `list`: Toont een lijst van alle releases in het cluster.
- `repo`: Beheert Helm-repositories.

## Veelvoorkomende voorbeelden

### 1. Een nieuwe release installeren
Om een nieuwe applicatie te installeren met Helm, gebruik je de volgende opdracht:

```bash
helm install mijn-app stable/mijn-chart
```

### 2. Een bestaande release upgraden
Om een bestaande release te upgraden naar een nieuwe versie, gebruik je:

```bash
helm upgrade mijn-app stable/mijn-chart
```

### 3. Een release verwijderen
Om een release uit het cluster te verwijderen, gebruik je:

```bash
helm uninstall mijn-app
```

### 4. Lijst van alle releases bekijken
Om een lijst van alle geïnstalleerde releases te bekijken, gebruik je:

```bash
helm list
```

### 5. Een nieuwe repository toevoegen
Om een nieuwe Helm-repository toe te voegen, gebruik je:

```bash
helm repo add mijn-repo https://example.com/charts
```

## Tips
- Zorg ervoor dat je altijd de laatste versie van Helm gebruikt voor de beste compatibiliteit en nieuwe functies.
- Gebruik `helm search` om beschikbare charts in repositories te vinden.
- Maak gebruik van waardenbestanden (`values.yaml`) om configuraties voor je charts te beheren en aan te passen.