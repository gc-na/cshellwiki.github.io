# [Linux] Bash continue utilizare: [continuă execuția unui script]

## Overview
Comanda `continue` în Bash este utilizată pentru a sări la următoarea iterație a unui ciclu, cum ar fi `for`, `while` sau `until`. Aceasta permite continuarea execuției fără a executa restul codului din interiorul buclei pentru iterația curentă.

## Usage
Sintaxa de bază a comenzii este:

```
continue [n]
```

Unde `n` este un număr opțional care specifică câte iterații trebuie să sară. Dacă `n` nu este specificat, se va sări la următoarea iterație.

## Common Options
- `n`: Sari la următoarea iterație a buclei, sărind `n` iterații. Dacă `n` este omis, se sare la următoarea iterație.

## Common Examples
### Exemplul 1: Sărirea la următoarea iterație
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo "Numărul este: $i"
done
```
**Ieșire:**
```
Numărul este: 1
Numărul este: 2
Numărul este: 4
Numărul este: 5
```

### Exemplul 2: Sărirea mai multor iterații
```bash
for i in {1..10}; do
  if [ $i -lt 5 ]; then
    continue 2
  fi
  echo "Numărul este: $i"
done
```
**Ieșire:**
```
Numărul este: 5
Numărul este: 6
Numărul este: 7
Numărul este: 8
Numărul este: 9
Numărul este: 10
```

### Exemplul 3: Utilizarea în bucle while
```bash
count=0
while [ $count -lt 5 ]; do
  count=$((count + 1))
  if [ $count -eq 3 ]; then
    continue
  fi
  echo "Contorul este: $count"
done
```
**Ieșire:**
```
Contorul este: 1
Contorul este: 2
Contorul este: 4
Contorul este: 5
```

## Tips
- Folosește `continue` cu grijă pentru a evita bucle infinite. Asigură-te că condițiile care duc la `continue` sunt bine definite.
- Este util să folosești `continue` în combinație cu condiții pentru a controla fluxul execuției în bucle complexe.
- Testează întotdeauna scripturile tale pentru a te asigura că logica de sărire funcționează așa cum te aștepți.