# [Linux] Bash kubectl användning: Hantera Kubernetes-kluster

## Översikt
`kubectl` är ett kommandoradsverktyg som används för att interagera med Kubernetes-kluster. Det gör det möjligt för användare att utföra olika operationer, såsom att skapa, uppdatera och ta bort resurser i klustret.

## Användning
Den grundläggande syntaxen för `kubectl` ser ut som följer:

```bash
kubectl [alternativ] [argument]
```

## Vanliga alternativ
- `get`: Hämtar resurser från klustret.
- `apply`: Tillämpa en konfiguration på resurser.
- `delete`: Tar bort resurser från klustret.
- `describe`: Visar detaljerad information om en resurs.
- `logs`: Visar loggar för en specifik pod.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `kubectl`:

1. **Hämta alla pods i det aktuella namnutrymmet:**
   ```bash
   kubectl get pods
   ```

2. **Skapa en resurs från en YAML-fil:**
   ```bash
   kubectl apply -f filnamn.yaml
   ```

3. **Ta bort en specifik pod:**
   ```bash
   kubectl delete pod pod-namn
   ```

4. **Visa detaljer om en tjänst:**
   ```bash
   kubectl describe service tjänst-namn
   ```

5. **Visa loggar för en pod:**
   ```bash
   kubectl logs pod-namn
   ```

## Tips
- Använd `kubectl get all` för att snabbt se alla resurser i det aktuella namnutrymmet.
- Använd `-n` för att specificera ett annat namnutrymme, till exempel `kubectl get pods -n namnutrymme`.
- För att få hjälp med kommandon kan du använda `kubectl --help` eller `kubectl [kommando] --help` för mer specifik hjälp.