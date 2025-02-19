# [Linux] C Shell (csh) gebruikerscommando: Toont actieve gebruikers

## Overzicht
Het `users` commando in C Shell (csh) toont een lijst van de gebruikers die momenteel zijn ingelogd op het systeem. Dit is handig voor systeembeheerders en gebruikers die willen weten wie er actief is op een bepaald moment.

## Gebruik
De basis syntaxis van het `users` commando is als volgt:

```
users [opties]
```

## Veelvoorkomende Opties
- `-n`: Toon het aantal unieke gebruikers in plaats van hun namen.
- `-r`: Toon alleen de gebruikers die een actieve sessie hebben.

## Veelvoorkomende Voorbeelden

1. **Toon alle ingelogde gebruikers:**
   ```csh
   users
   ```

2. **Toon het aantal unieke ingelogde gebruikers:**
   ```csh
   users -n
   ```

3. **Toon alleen actieve gebruikers:**
   ```csh
   users -r
   ```

## Tips
- Gebruik het `users` commando in combinatie met andere commando's zoals `who` of `w` voor meer gedetailleerde informatie over ingelogde gebruikers.
- Dit commando is handig voor het monitoren van systeemactiviteit, vooral op gedeelde systemen.