# [Linux] Bash break användning: Avsluta loopar

## Översikt
Kommandot `break` används i Bash-skript för att avsluta en loop tidigt. Det är användbart när du vill stoppa en loop baserat på ett specifikt villkor, snarare än att låta den köra till sitt naturliga slut.

## Användning
Den grundläggande syntaxen för kommandot `break` är:

```bash
break [n]
```

Där `n` är ett valfritt argument som anger hur många nivåer av loopar som ska avslutas. Om inget argument anges, avslutas endast den innersta loopen.

## Vanliga alternativ
- `n`: Anger hur många nivåer av loopar som ska avslutas. Om `n` är 1, avslutas endast den innersta loopen; om `n` är 2, avslutas den näst innersta loopen, och så vidare.

## Vanliga exempel

### Exempel 1: Avsluta en enkel loop
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
Detta skript kommer att skriva ut 1 och 2, och sedan avsluta loopen när `i` är 3.

### Exempel 2: Avsluta en while-loop
```bash
count=1
while true; do
  echo $count
  if [ $count -ge 5 ]; then
    break
  fi
  ((count++))
done
```
Här kommer loopen att skriva ut siffrorna 1 till 5 och sedan avsluta.

### Exempel 3: Avsluta en nästlad loop
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
Detta exempel avslutar både den inre och yttre loopen när `j` är 2.

## Tips
- Använd `break` för att förbättra effektiviteten i dina skript genom att undvika onödiga iterationer.
- Var medveten om hur många nivåer av loopar du vill avsluta när du använder argumentet `n`.
- Testa alltid dina skript med olika villkor för att säkerställa att `break` fungerar som förväntat.