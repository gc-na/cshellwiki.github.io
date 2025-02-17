# [Linux] Bash kubectl Bruk: Administrere Kubernetes-klynger

## Oversikt
`kubectl` er et kommandolinjeverktøy som brukes til å administrere Kubernetes-klynger. Det lar brukere utføre ulike operasjoner som å opprette, oppdatere og slette ressurser i klyngen.

## Bruk
Grunnleggende syntaks for `kubectl`-kommandoen er som følger:

```bash
kubectl [alternativer] [argumenter]
```

## Vanlige alternativer
- `get`: Hente ressurser fra klyngen.
- `apply`: Bruke en konfigurasjonsfil for å opprette eller oppdatere ressurser.
- `delete`: Slette ressurser fra klyngen.
- `describe`: Vise detaljer om en spesifikk ressurs.
- `logs`: Hente loggene til en pod.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `kubectl` kan brukes:

### Hente alle pods
```bash
kubectl get pods
```

### Oppdatere en ressurs med en YAML-fil
```bash
kubectl apply -f filnavn.yaml
```

### Slette en spesifikk pod
```bash
kubectl delete pod pod-navn
```

### Vise detaljer om en tjeneste
```bash
kubectl describe service tjeneste-navn
```

### Hente logger fra en pod
```bash
kubectl logs pod-navn
```

## Tips
- Bruk `kubectl get all` for å få en oversikt over alle ressurser i klyngen.
- Legg til `-n [navn-på-namespace]` for å spesifisere et namespace hvis du jobber med flere namespaces.
- Bruk `--watch`-alternativet for å overvåke endringer i ressurser i sanntid.