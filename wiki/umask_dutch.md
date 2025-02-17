# [Linux] Bash umask gebruik: Beheer van bestandspermissies

## Overview
De `umask`-opdracht in Bash wordt gebruikt om de standaard bestandspermissies in te stellen voor nieuwe bestanden en mappen die door een gebruiker worden aangemaakt. Het bepaalt welke rechten niet worden toegekend aan nieuwe bestanden en mappen.

## Usage
De basis syntaxis van de `umask`-opdracht is als volgt:

```bash
umask [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor `umask`:

- `-S`: Toont de umask in symbolische notatie.
- `-p`: Toont de huidige umask-waarde in een uitvoerbare vorm.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van `umask`:

1. **Toon de huidige umask-waarde:**
   ```bash
   umask
   ```

2. **Stel een nieuwe umask-waarde in (bijvoorbeeld 027):**
   ```bash
   umask 027
   ```

3. **Toon de umask-waarde in symbolische notatie:**
   ```bash
   umask -S
   ```

4. **Stel de umask in voor de huidige sessie:**
   ```bash
   umask 002
   ```

## Tips
- Het is een goede gewoonte om de umask-waarde in je shell-configuratiebestand (zoals `.bashrc` of `.bash_profile`) in te stellen, zodat deze automatisch wordt toegepast bij elke nieuwe sessie.
- Controleer regelmatig je umask-instellingen om ervoor te zorgen dat ze voldoen aan de beveiligingsvereisten van je systeem.
- Wees voorzichtig met het instellen van een te permissieve umask, omdat dit kan leiden tot ongewenste toegang tot je bestanden door andere gebruikers.