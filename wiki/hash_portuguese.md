# [Linux] Bash hash uso: Gerencia o cache de comandos

## Overview
O comando `hash` no Bash é utilizado para gerenciar o cache de comandos executados. Ele armazena os caminhos dos comandos que foram utilizados, permitindo que o shell os encontre mais rapidamente em execuções futuras.

## Usage
A sintaxe básica do comando `hash` é a seguinte:

```bash
hash [opções] [argumentos]
```

## Common Options
- `-r`: Limpa o cache de comandos, removendo todas as entradas armazenadas.
- `-p <comando>`: Define um caminho específico para um comando, substituindo a entrada atual no cache.
- `-l`: Lista todos os comandos armazenados no cache, mostrando seus caminhos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `hash`:

1. **Listar comandos armazenados no cache:**
   ```bash
   hash -l
   ```

2. **Limpar o cache de comandos:**
   ```bash
   hash -r
   ```

3. **Definir um caminho específico para um comando:**
   ```bash
   hash -p /usr/local/bin/meu_comando meu_comando
   ```

4. **Verificar o caminho de um comando específico:**
   ```bash
   hash ls
   ```

## Tips
- Utilize `hash -l` regularmente para verificar quais comandos estão armazenados em cache e seus respectivos caminhos.
- Após instalar novos programas, considere usar `hash -r` para garantir que o cache esteja atualizado e reflita as novas localizações dos comandos.
- Definir caminhos específicos com `-p` pode ser útil se você tiver versões diferentes de um comando em locais diferentes.