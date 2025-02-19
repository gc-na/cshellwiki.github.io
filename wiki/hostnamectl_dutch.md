# [Linux] C Shell (csh) hostnamectl gebruik: Beheer van systeemhostnamen

## Overzicht
Het `hostnamectl` commando wordt gebruikt om de hostnaam van een systeem te beheren en te configureren. Het biedt ook informatie over het systeem, zoals het besturingssysteem, de kernelversie en de hardware-informatie.

## Gebruik
De basis syntaxis van het `hostnamectl` commando is als volgt:

```csh
hostnamectl [opties] [argumenten]
```

## Veelvoorkomende Opties
- `set-hostname`: Wijzig de hostnaam van het systeem.
- `status`: Toon de huidige hostnaam en systeeminformatie.
- `set-icon-name`: Stel een pictogramnaam in voor de host.
- `set-chassis`: Stel het type chassis in (bijv. desktop, laptop).
- `set-deployment`: Stel de implementatie-informatie in.

## Veelvoorkomende Voorbeelden

### Huidige Hostnaam Bekijken
Om de huidige hostnaam en systeeminformatie te bekijken, gebruik je:

```csh
hostnamectl status
```

### Hostnaam Instellen
Om de hostnaam van het systeem te wijzigen, gebruik je:

```csh
hostnamectl set-hostname nieuwe-hostnaam
```

### Chassis Type Instellen
Om het type chassis in te stellen, gebruik je:

```csh
hostnamectl set-chassis laptop
```

### Pictogramnaam Instellen
Om een pictogramnaam in te stellen voor de host, gebruik je:

```csh
hostnamectl set-icon-name computer-laptop
```

## Tips
- Zorg ervoor dat je de juiste machtigingen hebt (meestal root) om de hostnaam te wijzigen.
- Controleer altijd de huidige hostnaam met `hostnamectl status` voordat je wijzigingen aanbrengt.
- Na het wijzigen van de hostnaam, kan het nodig zijn om je systeem opnieuw op te starten om de wijzigingen volledig door te voeren.