# [Linux] Bash flatpak gebruik: Beheer van applicaties in sandboxed omgevingen

## Overview
De `flatpak`-opdracht is een hulpmiddel voor het installeren, uitvoeren en beheren van applicaties in een sandboxed omgeving. Dit zorgt ervoor dat applicaties veilig en onafhankelijk van het besturingssysteem kunnen draaien, wat de compatibiliteit en beveiliging verbetert.

## Usage
De basis syntaxis van de `flatpak`-opdracht is als volgt:

```bash
flatpak [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor de `flatpak`-opdracht:

- `install`: Installeert een Flatpak-applicatie.
- `run`: Voert een geïnstalleerde Flatpak-applicatie uit.
- `remove`: Verwijdert een geïnstalleerde Flatpak-applicatie.
- `list`: Toont een lijst van geïnstalleerde Flatpak-applicaties.
- `update`: Werk geïnstalleerde Flatpak-applicaties bij naar de nieuwste versie.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van de `flatpak`-opdracht:

1. **Een applicatie installeren:**
   ```bash
   flatpak install flathub org.videolan.VLC
   ```

2. **Een applicatie uitvoeren:**
   ```bash
   flatpak run org.videolan.VLC
   ```

3. **Een applicatie verwijderen:**
   ```bash
   flatpak remove org.videolan.VLC
   ```

4. **Een lijst van geïnstalleerde applicaties bekijken:**
   ```bash
   flatpak list
   ```

5. **Geïnstalleerde applicaties bijwerken:**
   ```bash
   flatpak update
   ```

## Tips
- Zorg ervoor dat je de juiste repository hebt toegevoegd voordat je een applicatie installeert. De meeste populaire applicaties zijn beschikbaar in de `flathub` repository.
- Gebruik `flatpak info [applicatie]` om meer informatie over een specifieke applicatie te krijgen, zoals de versie en de geïnstalleerde runtime.
- Het is handig om regelmatig je Flatpak-applicaties bij te werken om beveiligingspatches en nieuwe functies te ontvangen.