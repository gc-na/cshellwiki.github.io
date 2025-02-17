# [Linux] Bash schrijf: Berichten naar andere gebruikers verzenden

## Overzicht
De `write` opdracht in Bash stelt gebruikers in staat om tekstberichten naar andere ingelogde gebruikers op hetzelfde systeem te verzenden. Dit kan handig zijn voor directe communicatie zonder gebruik te maken van e-mail of andere messaging-applicaties.

## Gebruik
De basis syntaxis van de `write` opdracht is als volgt:

```bash
write [opties] [gebruiker] [tty]
```

Hierbij is `[gebruiker]` de naam van de gebruiker naar wie je een bericht wilt sturen, en `[tty]` is de terminal waarop de gebruiker is ingelogd (optioneel).

## Veelvoorkomende Opties
- `-n`: Schakel de echo van de verzonden berichten uit.
- `-h`: Geef een korte helptekst weer.

## Veelvoorkomende Voorbeelden

1. Een bericht sturen naar een gebruiker:
   ```bash
   write jan
   Dit is een testbericht.
   ```

2. Een bericht sturen naar een specifieke terminal van een gebruiker:
   ```bash
   write jan pts/1
   Hallo Jan, hoe gaat het?
   ```

3. Gebruik maken van de optie om echo uit te schakelen:
   ```bash
   write -n jan
   Dit bericht wordt niet weergegeven op mijn terminal.
   ```

## Tips
- Zorg ervoor dat de ontvanger de `mesg` opdracht heeft ingesteld op `y` om berichten te kunnen ontvangen.
- Gebruik `Ctrl + D` om het bericht te beëindigen en te verzenden.
- Houd je berichten kort en duidelijk om verwarring te voorkomen.