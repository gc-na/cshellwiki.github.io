# [Linux] Bash minikube Χρήση: Δημιουργία τοπικών Kubernetes clusters

## Overview
Η εντολή `minikube` χρησιμοποιείται για τη δημιουργία και τη διαχείριση τοπικών Kubernetes clusters. Είναι ένα εργαλείο που διευκολύνει την ανάπτυξη και τη δοκιμή εφαρμογών σε περιβάλλον Kubernetes, επιτρέποντας στους προγραμματιστές να εργάζονται τοπικά.

## Usage
Η βασική σύνταξη της εντολής είναι η εξής:

```bash
minikube [options] [arguments]
```

## Common Options
- `start`: Ξεκινά ένα νέο minikube cluster.
- `stop`: Σταματά το τρέχον cluster.
- `delete`: Διαγράφει το cluster.
- `status`: Εμφανίζει την κατάσταση του cluster.
- `kubectl`: Επιτρέπει την εκτέλεση εντολών kubectl στο minikube cluster.

## Common Examples
- Ξεκινήστε ένα νέο minikube cluster:
  ```bash
  minikube start
  ```

- Σταματήστε το τρέχον cluster:
  ```bash
  minikube stop
  ```

- Διαγράψτε το cluster:
  ```bash
  minikube delete
  ```

- Ελέγξτε την κατάσταση του cluster:
  ```bash
  minikube status
  ```

- Χρησιμοποιήστε το kubectl για να εκτελέσετε εντολές στο cluster:
  ```bash
  kubectl get pods --all-namespaces
  ```

## Tips
- Βεβαιωθείτε ότι έχετε εγκαταστήσει τις απαιτούμενες εξαρτήσεις, όπως το VirtualBox ή το Docker, πριν ξεκινήσετε το minikube.
- Χρησιμοποιήστε την επιλογή `--driver` για να επιλέξετε τον κατάλληλο οδηγό εικονικοποίησης για το σύστημά σας.
- Ελέγξτε τα logs του minikube με την εντολή `minikube logs` για να διαγνώσετε τυχόν προβλήματα.