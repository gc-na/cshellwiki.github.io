# [Linux] C Shell (csh) hostnamectl Verwendung: Systemhostname verwalten

## Übersicht
Der Befehl `hostnamectl` wird verwendet, um den Hostnamen eines Systems zu verwalten und anzuzeigen. Er ermöglicht es Benutzern, den aktuellen Hostnamen zu ändern, Informationen über das System abzurufen und die Netzwerkkonfiguration zu überprüfen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
hostnamectl [Optionen] [Argumente]
```

## Häufige Optionen
- `set-hostname`: Ändert den aktuellen Hostnamen des Systems.
- `status`: Zeigt den aktuellen Hostnamen und andere relevante Systeminformationen an.
- `set-icon-name`: Setzt den Symbolnamen für den Host.
- `set-chassis`: Legt den Chassis-Typ des Systems fest (z. B. "desktop", "laptop").

## Häufige Beispiele
- Um den aktuellen Hostnamen anzuzeigen:

```csh
hostnamectl status
```

- Um den Hostnamen auf "mein-server" zu ändern:

```csh
hostnamectl set-hostname mein-server
```

- Um den Chassis-Typ auf "laptop" zu setzen:

```csh
hostnamectl set-chassis laptop
```

- Um den Symbolnamen auf "computer" zu setzen:

```csh
hostnamectl set-icon-name computer
```

## Tipps
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen, um den Hostnamen zu ändern; in der Regel sind Administratorrechte erforderlich.
- Überprüfen Sie nach der Änderung des Hostnamens, ob alle Dienste korrekt funktionieren, da einige Dienste möglicherweise den Hostnamen benötigen.
- Verwenden Sie `hostnamectl status`, um eine Übersicht über die aktuellen Systemeinstellungen zu erhalten, bevor Sie Änderungen vornehmen.