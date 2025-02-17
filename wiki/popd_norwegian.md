# [Linux] Bash popd bruk: Gå tilbake til tidligere katalog

## Oversikt
`popd`-kommandoen brukes til å bytte tilbake til den tidligere katalogen som er lagret i katalogstakken. Dette er nyttig når du har navigert gjennom flere kataloger og ønsker å gå tilbake til en tidligere posisjon uten å måtte skrive inn hele stien.

## Bruk
Grunnleggende syntaks for `popd`-kommandoen er som følger:

```bash
popd [alternativer]
```

## Vanlige alternativer
- `+n`: Gå tilbake til katalogen som er n posisjoner fra toppen av stakken.
- `-n`: Gå tilbake til katalogen som er n posisjoner fra bunnen av stakken.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `popd` kan brukes:

### Eksempel 1: Gå tilbake til den forrige katalogen
```bash
cd /home/user/Documents
cd /home/user/Downloads
popd
```
I dette eksemplet vil `popd` ta deg tilbake til `/home/user/Documents`.

### Eksempel 2: Bruke katalogstakken
```bash
pushd /var/log
pushd /etc
popd
```
Her vil `popd` ta deg tilbake til `/var/log`, som var den forrige katalogen før du gikk til `/etc`.

### Eksempel 3: Gå tilbake til en spesifikk posisjon
```bash
pushd /usr/local
pushd /usr/bin
popd +1
```
I dette tilfellet vil `popd +1` ta deg tilbake til `/usr/local`, som er en posisjon lenger ned i stakken.

## Tips
- Bruk `pushd` sammen med `popd` for effektiv navigering mellom kataloger.
- Sjekk innholdet i katalogstakken med `dirs` for å se hvilke kataloger som er lagret.
- Vær oppmerksom på at `popd` vil fjerne den øverste katalogen fra stakken, så vær sikker på at du ikke trenger den før du bruker kommandoen.