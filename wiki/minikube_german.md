# [Linux] Bash minikube Verwendung: Lokale Kubernetes-Cluster erstellen

## Übersicht
Der `minikube` Befehl wird verwendet, um lokale Kubernetes-Cluster auf Ihrem Rechner zu erstellen und zu verwalten. Es ist ein nützliches Werkzeug für Entwickler, die Kubernetes-Anwendungen testen und entwickeln möchten, ohne eine vollständige Cloud-Umgebung einrichten zu müssen.

## Verwendung
Die grundlegende Syntax des `minikube` Befehls lautet:

```bash
minikube [Optionen] [Argumente]
```

## Häufige Optionen
- `start`: Startet ein neues Minikube-Cluster.
- `stop`: Stoppt das laufende Minikube-Cluster.
- `delete`: Löscht das Minikube-Cluster.
- `status`: Zeigt den Status des Minikube-Clusters an.
- `dashboard`: Öffnet das Kubernetes-Dashboard im Browser.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `minikube`:

1. **Minikube-Cluster starten:**
   ```bash
   minikube start
   ```

2. **Minikube-Cluster stoppen:**
   ```bash
   minikube stop
   ```

3. **Minikube-Cluster löschen:**
   ```bash
   minikube delete
   ```

4. **Status des Minikube-Clusters überprüfen:**
   ```bash
   minikube status
   ```

5. **Kubernetes-Dashboard öffnen:**
   ```bash
   minikube dashboard
   ```

## Tipps
- Stellen Sie sicher, dass Ihr System die erforderlichen Virtualisierungsfunktionen unterstützt, bevor Sie Minikube verwenden.
- Verwenden Sie den Befehl `minikube addons list`, um verfügbare Add-ons zu sehen und diese bei Bedarf zu aktivieren.
- Nutzen Sie `minikube config set`, um Konfigurationseinstellungen für Ihr Cluster anzupassen, wie z.B. die verwendete Kubernetes-Version.