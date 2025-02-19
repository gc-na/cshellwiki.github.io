# [Linux] C Shell (csh) schrijf: Berichten naar andere gebruikers verzenden

## Overzicht
De `write`-opdracht in C Shell (csh) stelt gebruikers in staat om directe berichten naar andere ingelogde gebruikers op hetzelfde systeem te sturen. Dit kan handig zijn voor communicatie zonder gebruik te maken van e-mail of andere messaging-applicaties.

## Gebruik
De basis syntaxis van de `write`-opdracht is als volgt:

```csh
write [opties] [gebruiker]
```

## Veelvoorkomende Opties
- `-n`: Schakel de prompt voor het invoeren van een bericht uit.
- `-h`: Toon een helpbericht met informatie over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden

1. Een bericht sturen naar een specifieke gebruiker:
   ```csh
   write jan
   Dit is een testbericht.
   ```

2. Een bericht sturen zonder een prompt te tonen:
   ```csh
   write -n jan
   Dit is een stil bericht.
   ```

3. Een bericht sturen naar een gebruiker met een specifieke terminal:
   ```csh
   write jan pts/1
   Hallo Jan, hoe gaat het?
   ```

## Tips
- Zorg ervoor dat de ontvanger is ingelogd en de terminal niet in de 'niet storen'-modus staat om het bericht te ontvangen.
- Gebruik `who` of `w` om te controleren welke gebruikers ingelogd zijn voordat je een bericht verzendt.
- Wees kort en duidelijk in je berichten om verwarring te voorkomen.