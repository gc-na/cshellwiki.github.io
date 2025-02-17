# [Linux] Bash yum användning: Hantera paket på ett enkelt sätt

## Översikt
`yum` (Yellowdog Updater, Modified) är en pakethanterare för Linux-distributioner som använder RPM-paketformatet. Den används för att installera, uppgradera, ta bort och hantera programvara på systemet.

## Användning
Den grundläggande syntaxen för `yum`-kommandot är:

```bash
yum [alternativ] [argument]
```

## Vanliga alternativ
- `install`: Installerar ett paket.
- `remove`: Tar bort ett paket.
- `update`: Uppdaterar installerade paket till den senaste versionen.
- `search`: Söker efter paket i repository.
- `info`: Visar information om ett specifikt paket.
- `list`: Visar en lista över installerade eller tillgängliga paket.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `yum`:

### Installera ett paket
För att installera ett paket, till exempel `wget`, kan du använda följande kommando:

```bash
yum install wget
```

### Ta bort ett paket
För att ta bort ett installerat paket, till exempel `wget`, använder du:

```bash
yum remove wget
```

### Uppdatera alla paket
För att uppdatera alla installerade paket till den senaste versionen, kör:

```bash
yum update
```

### Söka efter ett paket
För att söka efter ett paket, till exempel `httpd`, kan du använda:

```bash
yum search httpd
```

### Visa information om ett paket
För att få information om ett specifikt paket, exempelvis `httpd`, använd:

```bash
yum info httpd
```

## Tips
- Använd `yum clean all` för att rensa cache och frigöra utrymme.
- Kontrollera alltid tillgängliga uppdateringar regelbundet för att hålla systemet säkert och uppdaterat.
- Använd `yum list installed` för att se alla installerade paket på ditt system.