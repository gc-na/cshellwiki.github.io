# [Linux] C Shell (csh) chage gebruik: Beheer gebruikerswachtwoordverval

## Overzicht
De `chage`-opdracht wordt gebruikt om de wachtwoordvervalinstellingen voor gebruikersaccounts in een Linux-systeem te beheren. Hiermee kunt u de tijdsduur instellen voordat een gebruiker zijn wachtwoord moet wijzigen, evenals andere gerelateerde parameters.

## Gebruik
De basisstructuur van de `chage`-opdracht is als volgt:

```bash
chage [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l, --list`: Toon de huidige instellingen voor de gebruiker.
- `-m, --mindays`: Stel het minimum aantal dagen in tussen wachtwoordwijzigingen.
- `-M, --maxdays`: Stel het maximum aantal dagen in dat een wachtwoord geldig is.
- `-I, --inactive`: Stel het aantal dagen in dat een account inactief blijft na het verlopen van het wachtwoord.
- `-E, --expire`: Stel de datum in waarop het account vervalt.

## Veelvoorkomende Voorbeelden
- **Toon de huidige wachtwoordinstellingen voor een gebruiker:**
  ```bash
  chage -l gebruikersnaam
  ```

- **Stel het minimum aantal dagen in tussen wachtwoordwijzigingen op 7 dagen:**
  ```bash
  chage -m 7 gebruikersnaam
  ```

- **Stel het maximum aantal dagen in dat een wachtwoord geldig is op 90 dagen:**
  ```bash
  chage -M 90 gebruikersnaam
  ```

- **Stel de inactiviteitsperiode in op 30 dagen:**
  ```bash
  chage -I 30 gebruikersnaam
  ```

- **Stel de vervaldatum van het account in op 2023-12-31:**
  ```bash
  chage -E 2023-12-31 gebruikersnaam
  ```

## Tips
- Controleer regelmatig de wachtwoordinstellingen van gebruikers om de beveiliging van uw systeem te waarborgen.
- Gebruik de `-l` optie om een overzicht te krijgen van de instellingen voordat u wijzigingen aanbrengt.
- Wees voorzichtig met het instellen van een vervaldatum, omdat dit kan leiden tot onbereikbare accounts als gebruikers niet op tijd hun wachtwoord wijzigen.