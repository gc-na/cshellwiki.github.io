# [Linux] Bash renice användning: Ändra prioritet för processer

## Översikt
Kommandot `renice` används för att ändra prioriteten för en eller flera processer som körs på systemet. Genom att justera prioriteten kan användare styra hur mycket CPU-resurser en process får, vilket kan vara användbart för att optimera systemets prestanda.

## Användning
Den grundläggande syntaxen för kommandot `renice` är:

```
renice [alternativ] [prioritet] [PID...]
```

## Vanliga alternativ
- `-n` : Anger den nya prioriteten.
- `-g` : Ändrar prioriteten för alla processer som tillhör en specifik grupp.
- `-p` : Anger att prioriteten ska ändras för en specifik process genom att ange dess PID (Process ID).

## Vanliga exempel
Här är några praktiska exempel på hur man använder `renice`:

1. Ändra prioriteten för en specifik process:
   ```bash
   renice -n 10 -p 1234
   ```
   Detta kommando ändrar prioriteten för processen med PID 1234 till 10.

2. Ändra prioriteten för flera processer:
   ```bash
   renice -n 5 -p 1234 5678
   ```
   Här ändras prioriteten för både processerna med PID 1234 och 5678 till 5.

3. Ändra prioriteten för alla processer i en specifik grupp:
   ```bash
   renice -n -5 -g 1000
   ```
   Detta kommando sätter prioriteten för alla processer som tillhör gruppen med GID 1000 till -5.

## Tips
- Kontrollera nuvarande prioritet för en process med kommandot `ps` innan du använder `renice`.
- Använd negativa värden för att öka prioriteten och positiva värden för att minska den.
- Var försiktig med att ändra prioriteten för systemprocesser, eftersom det kan påverka systemets stabilitet och prestanda.