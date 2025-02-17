# [Λειτουργικό Σύστημα] Bash kubectl Χρήση: Διαχείριση πόρων Kubernetes

## Overview
Η εντολή `kubectl` είναι το εργαλείο γραμμής εντολών που χρησιμοποιείται για την αλληλεπίδραση με το Kubernetes. Επιτρέπει στους χρήστες να διαχειρίζονται πόρους, να εκτελούν εντολές και να παρακολουθούν την κατάσταση των εφαρμογών που τρέχουν σε ένα cluster Kubernetes.

## Usage
Η βασική σύνταξη της εντολής `kubectl` είναι η εξής:

```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: Λαμβάνει πληροφορίες για πόρους.
- `apply`: Εφαρμόζει αλλαγές σε πόρους από αρχεία YAML ή JSON.
- `delete`: Διαγράφει πόρους.
- `describe`: Παρέχει λεπτομέρειες για έναν συγκεκριμένο πόρο.
- `logs`: Εμφανίζει τα logs ενός pod.

## Common Examples
### 1. Λήψη λίστας pods
```bash
kubectl get pods
```

### 2. Εφαρμογή αλλαγών από αρχείο YAML
```bash
kubectl apply -f deployment.yaml
```

### 3. Διαγραφή ενός pod
```bash
kubectl delete pod my-pod
```

### 4. Περιγραφή ενός service
```bash
kubectl describe service my-service
```

### 5. Εμφάνιση logs ενός pod
```bash
kubectl logs my-pod
```

## Tips
- Χρησιμοποιήστε την επιλογή `-n` για να καθορίσετε το namespace αν εργάζεστε με πολλαπλά namespaces.
- Ελέγξτε την κατάσταση των πόρων σας με την εντολή `kubectl get all` για μια συνολική εικόνα.
- Μάθετε να χρησιμοποιείτε aliases για συχνές εντολές για να εξοικονομήσετε χρόνο.