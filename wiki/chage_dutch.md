# [Linux] Bash chage gebruik: Beheer gebruikerswachtwoordverval

## Overzicht
Het `chage`-commando in Bash wordt gebruikt om de wachtwoordvervalinstellingen van gebruikersaccounts op een Linux-systeem te beheren. Hiermee kan een systeembeheerder de periode instellen waarin een wachtwoord moet worden gewijzigd en andere gerelateerde instellingen.

## Gebruik
De basis syntaxis van het `chage`-commando is als volgt:

```bash
chage [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l, --list`: Toon de huidige wachtwoordinstellingen voor een gebruiker.
- `-m, --mindays`: Stel het minimum aantal dagen in tussen wachtwoordwijzigingen.
- `-M, --maxdays`: Stel het maximum aantal dagen in voordat een wachtwoord moet worden gewijzigd.
- `-I, --inactive`: Stel het aantal dagen in dat een account inactief blijft na het verlopen van het wachtwoord.
- `-E, --expire`: Stel de datum in waarop het account verloopt.

## Veelvoorkomende voorbeelden

1. **Toon de wachtwoordinstellingen voor een gebruiker:**
   ```bash
   chage -l username
   ```

2. **Stel het minimum aantal dagen in tussen wachtwoordwijzigingen op 5 dagen:**
   ```bash
   chage -m 5 username
   ```

3. **Stel het maximum aantal dagen in voordat een wachtwoord moet worden gewijzigd op 90 dagen:**
   ```bash
   chage -M 90 username
   ```

4. **Stel het aantal inactieve dagen in op 30 dagen na het verlopen van het wachtwoord:**
   ```bash
   chage -I 30 username
   ```

5. **Stel de vervaldatum van het account in op 2024-12-31:**
   ```bash
   chage -E 2024-12-31 username
   ```

## Tips
- Zorg ervoor dat je het `chage`-commando uitvoert met root- of sudo-rechten om wijzigingen aan gebruikersaccounts aan te brengen.
- Controleer regelmatig de wachtwoordinstellingen van gebruikers om de beveiliging van je systeem te waarborgen.
- Gebruik de `-l` optie om een overzicht te krijgen van de huidige instellingen voordat je wijzigingen aanbrengt.