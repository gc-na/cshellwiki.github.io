# [Linux] Bash hostnamectl gebruik: Beheer van systeemhostnamen

## Overzicht
Het `hostnamectl` commando wordt gebruikt om de hostnaam van een systeem te beheren en informatie over het systeem weer te geven. Het is een onderdeel van systemd en biedt een eenvoudige manier om de hostnaam en gerelateerde instellingen te configureren.

## Gebruik
De basis syntaxis van het `hostnamectl` commando is als volgt:

```bash
hostnamectl [opties] [argumenten]
```

## Veelvoorkomende Opties
- `set-hostname`: Wijzigt de hostnaam van het systeem.
- `status`: Toont de huidige hostnaam en andere systeeminformatie.
- `set-icon-name`: Stelt een pictogramnaam in voor de host.
- `set-chassis`: Stelt het type chassis in (bijv. desktop, laptop).

## Veelvoorkomende Voorbeelden

### 1. Huidige hostnaam weergeven
Om de huidige hostnaam en systeeminformatie weer te geven, gebruik je:

```bash
hostnamectl status
```

### 2. Hostnaam instellen
Om de hostnaam van het systeem te wijzigen, gebruik je:

```bash
sudo hostnamectl set-hostname nieuwe-hostnaam
```

### 3. Chassis type instellen
Om het chassis type in te stellen, gebruik je:

```bash
sudo hostnamectl set-chassis laptop
```

### 4. Pictogramnaam instellen
Om een pictogramnaam in te stellen, gebruik je:

```bash
sudo hostnamectl set-icon-name computer-laptop
```

## Tips
- Zorg ervoor dat je het commando met `sudo` uitvoert als je wijzigingen aanbrengt aan de hostnaam of systeeminstellingen.
- Controleer altijd de huidige hostnaam met `hostnamectl status` voordat je wijzigingen aanbrengt.
- Na het wijzigen van de hostnaam kan het nodig zijn om je systeem opnieuw op te starten om de wijzigingen volledig door te voeren.