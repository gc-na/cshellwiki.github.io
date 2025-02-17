# [Linux] Bash usermod gebruik: Beheer gebruikersaccounts

## Overzicht
De `usermod`-opdracht in Bash wordt gebruikt om bestaande gebruikersaccounts op een Linux-systeem te wijzigen. Hiermee kunnen systeembeheerders verschillende eigenschappen van een gebruiker aanpassen, zoals hun groepslidmaatschappen, home directory en shell.

## Gebruik
De basis syntaxis van de `usermod`-opdracht is als volgt:

```bash
usermod [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-aG`: Voeg de gebruiker toe aan de gespecificeerde groepen zonder de huidige groepslidmaatschappen te verwijderen.
- `-d`: Wijzig de home directory van de gebruiker.
- `-s`: Wijzig de standaard shell van de gebruiker.
- `-L`: Vergrendel het account van de gebruiker.
- `-U`: Ontgrendel het account van de gebruiker.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `usermod`-opdracht:

### Voorbeeld 1: Voeg een gebruiker toe aan een groep
```bash
usermod -aG sudo gebruiker
```
Dit voegt de gebruiker "gebruiker" toe aan de "sudo" groep, waardoor ze beheerdersrechten krijgen.

### Voorbeeld 2: Wijzig de home directory van een gebruiker
```bash
usermod -d /nieuwe/home/directory gebruiker
```
Dit wijzigt de home directory van de gebruiker "gebruiker" naar "/nieuwe/home/directory".

### Voorbeeld 3: Wijzig de standaard shell van een gebruiker
```bash
usermod -s /bin/zsh gebruiker
```
Dit stelt de standaard shell van de gebruiker "gebruiker" in op Zsh.

### Voorbeeld 4: Vergrendel een gebruikersaccount
```bash
usermod -L gebruiker
```
Dit vergrendelt het account van de gebruiker "gebruiker", waardoor ze zich niet meer kunnen aanmelden.

### Voorbeeld 5: Ontgrendel een gebruikersaccount
```bash
usermod -U gebruiker
```
Dit ontgrendelt het account van de gebruiker "gebruiker", waardoor ze zich weer kunnen aanmelden.

## Tips
- Zorg ervoor dat je de juiste opties gebruikt om onbedoelde wijzigingen aan gebruikersaccounts te voorkomen.
- Gebruik de `-aG` optie altijd wanneer je een gebruiker aan een groep toevoegt, om te voorkomen dat ze uit andere groepen worden verwijderd.
- Controleer altijd de huidige instellingen van een gebruiker voordat je wijzigingen aanbrengt, bijvoorbeeld met de `id` of `getent passwd` opdrachten.