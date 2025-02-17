# [Linux] Bash minikube brug: Administrer lokale Kubernetes-klynger

## Oversigt
Minikube er et værktøj, der gør det muligt at køre en lokal Kubernetes-klynge. Det er ideelt til udvikling og test, da det giver en nem måde at oprette og administrere Kubernetes-miljøer på din egen maskine.

## Brug
Den grundlæggende syntaks for minikube-kommandoen er:

```bash
minikube [options] [arguments]
```

## Almindelige muligheder
- `start`: Starter en ny minikube-klynge.
- `stop`: Stopper den kørende minikube-klynge.
- `delete`: Sletter den eksisterende minikube-klynge.
- `status`: Viser status for minikube-klyngen.
- `kubectl`: Udfører kubectl-kommandoer på minikube-klyngen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger minikube:

1. **Starte en ny minikube-klynge:**
   ```bash
   minikube start
   ```

2. **Stoppe den kørende minikube-klynge:**
   ```bash
   minikube stop
   ```

3. **Slette minikube-klyngen:**
   ```bash
   minikube delete
   ```

4. **Tjekke status for minikube-klyngen:**
   ```bash
   minikube status
   ```

5. **Udføre en kubectl-kommando:**
   ```bash
   minikube kubectl -- get pods -A
   ```

## Tips
- Sørg for at have de nødvendige systemkrav opfyldt, før du starter minikube.
- Brug `minikube dashboard` for at åbne et webbaseret dashboard til at overvåge din klynge.
- Overvej at bruge forskellige drivere (f.eks. VirtualBox, Docker) afhængigt af dit system for bedre ydeevne.