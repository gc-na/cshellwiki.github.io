# [Linux] Bash kubectl brug: Administrer Kubernetes ressourcer

## Oversigt
`kubectl` er kommandolinjeværktøjet til at interagere med Kubernetes-klynger. Det giver brugerne mulighed for at udføre operationer som at oprette, opdatere, slette og overvåge ressourcer i en Kubernetes-implementering.

## Brug
Den grundlæggende syntaks for `kubectl` er som følger:

```bash
kubectl [options] [arguments]
```

## Almindelige muligheder
- `get`: Hent ressourcer fra klyngen.
- `apply`: Anvend ændringer på ressourcer.
- `delete`: Slet ressourcer fra klyngen.
- `describe`: Vis detaljer om en ressource.
- `logs`: Vis logfiler for en pod.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `kubectl` kan bruges:

1. Hent alle pods i den aktuelle namespace:
   ```bash
   kubectl get pods
   ```

2. Anvend en konfigurationsfil til at oprette eller opdatere ressourcer:
   ```bash
   kubectl apply -f deployment.yaml
   ```

3. Slet en specifik pod:
   ```bash
   kubectl delete pod my-pod
   ```

4. Vis detaljer om en specifik service:
   ```bash
   kubectl describe service my-service
   ```

5. Se logfiler for en pod:
   ```bash
   kubectl logs my-pod
   ```

## Tips
- Brug `kubectl get all` for hurtigt at se alle ressourcer i den aktuelle namespace.
- Tilføj `-n <namespace>` for at specificere en anden namespace.
- Brug `--watch` med `get` for at overvåge ændringer i realtid.
- Gem ofte brugte kommandoer i en shell-script for at automatisere opgaver.