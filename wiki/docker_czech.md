# [Linux] Bash docker použití: Správa kontejnerů a obrazů

## Přehled
Příkaz `docker` slouží k vytváření, správě a provozování kontejnerizovaných aplikací. Docker umožňuje vývojářům balit aplikace do kontejnerů, které obsahují všechny potřebné závislosti, což usnadňuje nasazení a škálování aplikací.

## Použití
Základní syntaxe příkazu je následující:

```bash
docker [možnosti] [argumenty]
```

## Běžné možnosti
- `run`: Spustí nový kontejner.
- `ps`: Zobrazí běžící kontejnery.
- `images`: Zobrazí dostupné obrazy.
- `pull`: Stáhne obraz z Docker Hub.
- `build`: Vytvoří obraz z Dockerfile.
- `rm`: Odstraní jeden nebo více kontejnerů.

## Běžné příklady
1. **Spuštění nového kontejneru**:
   ```bash
   docker run hello-world
   ```

2. **Zobrazení běžících kontejnerů**:
   ```bash
   docker ps
   ```

3. **Stáhnout obraz z Docker Hub**:
   ```bash
   docker pull ubuntu
   ```

4. **Vytvoření obrazu z Dockerfile**:
   ```bash
   docker build -t my-image .
   ```

5. **Odstranění kontejneru**:
   ```bash
   docker rm my-container
   ```

## Tipy
- Používejte `docker-compose` pro správu více kontejnerů a jejich vzájemné propojení.
- Pravidelně aktualizujte obrazy pomocí `docker pull`, abyste měli nejnovější verze.
- Vždy používejte specifické tagy pro obrazy, abyste se vyhnuli nechtěným aktualizacím.