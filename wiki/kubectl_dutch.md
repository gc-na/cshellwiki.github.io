# [Linux] Bash kubectl gebruik: Beheer Kubernetes-clusters

## Overzicht
De `kubectl`-opdracht is een krachtige commandoregeltool die wordt gebruikt om te communiceren met Kubernetes-clusters. Het stelt gebruikers in staat om verschillende taken uit te voeren, zoals het beheren van applicaties, het controleren van de status van resources en het uitvoeren van configuratiewijzigingen.

## Gebruik
De basis syntaxis van de `kubectl`-opdracht is als volgt:

```bash
kubectl [opties] [argumenten]
```

## Veelvoorkomende opties
- `get`: Haal informatie op over Kubernetes-resources.
- `apply`: Pas configuraties toe op resources.
- `delete`: Verwijder Kubernetes-resources.
- `describe`: Geef gedetailleerde informatie over een specifieke resource.
- `logs`: Bekijk de logbestanden van een pod.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `kubectl`:

1. **Lijst alle pods in de huidige namespace:**
   ```bash
   kubectl get pods
   ```

2. **Toepassen van een configuratiebestand:**
   ```bash
   kubectl apply -f configuratie.yaml
   ```

3. **Verwijder een specifieke pod:**
   ```bash
   kubectl delete pod naam-van-pod
   ```

4. **Bekijk de logs van een specifieke pod:**
   ```bash
   kubectl logs naam-van-pod
   ```

5. **Geef gedetailleerde informatie over een service:**
   ```bash
   kubectl describe service naam-van-service
   ```

## Tips
- Gebruik de `--namespace` optie om resources in een specifieke namespace te beheren.
- Maak gebruik van de `-o` optie om de uitvoer in verschillende indelingen te krijgen, zoals JSON of YAML.
- Houd je `kubectl`-versie up-to-date om te profiteren van de nieuwste functies en bugfixes.
- Gebruik `kubectl get all` om een overzicht te krijgen van alle resources in de huidige namespace.