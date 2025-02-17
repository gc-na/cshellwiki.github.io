# [Română] Bash docker utilizare: Gestionarea containerelor

## Overview
Docker este un instrument folosit pentru a automatiza desfășurarea aplicațiilor în containere. Aceste containere sunt unități standardizate care includ tot ce este necesar pentru a rula o aplicație, inclusiv codul, bibliotecile și dependențele.

## Usage
Sintaxa de bază a comenzii docker este:

```bash
docker [opțiuni] [argumente]
```

## Common Options
- `run`: Rulează un container nou.
- `ps`: Listează containerele active.
- `stop`: Oprește un container în execuție.
- `rm`: Șterge un container.
- `images`: Listează imaginile disponibile pe sistem.

## Common Examples
1. **Rularea unui container**:
   ```bash
   docker run hello-world
   ```
   Acest comand va descărca și va rula o imagine de testare.

2. **Listarea containerelor active**:
   ```bash
   docker ps
   ```
   Aceasta va afișa toate containerele care sunt în execuție.

3. **Oprirea unui container**:
   ```bash
   docker stop [container_id]
   ```
   Înlocuiți `[container_id]` cu ID-ul containerului pe care doriți să-l opriți.

4. **Ștergerea unui container**:
   ```bash
   docker rm [container_id]
   ```
   Aceasta va șterge un container specificat.

5. **Listarea imaginilor disponibile**:
   ```bash
   docker images
   ```
   Aceasta va afișa toate imaginile disponibile pe sistemul local.

## Tips
- Asigurați-vă că containerul este oprit înainte de a-l șterge.
- Utilizați `docker-compose` pentru a gestiona aplicații multi-container.
- Verificați regulat imaginile și containerele neutilizate pentru a economisi spațiu pe disc.