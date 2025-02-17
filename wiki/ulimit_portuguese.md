# [Linux] Bash ulimit Uso: Limitar recursos do sistema

## Overview
O comando `ulimit` é utilizado para definir ou exibir limites de recursos para processos em um shell. Isso é útil para controlar o uso de recursos do sistema, como a quantidade de memória ou o número máximo de arquivos abertos, evitando que um único processo consuma todos os recursos disponíveis.

## Usage
A sintaxe básica do comando `ulimit` é a seguinte:

```bash
ulimit [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `ulimit`:

- `-a`: Exibe todos os limites atuais.
- `-c`: Define o tamanho máximo do arquivo de core dump.
- `-d`: Define o tamanho máximo da memória do segmento de dados.
- `-f`: Define o tamanho máximo dos arquivos que podem ser criados.
- `-l`: Define o tamanho máximo da memória bloqueada.
- `-n`: Define o número máximo de descritores de arquivo abertos.
- `-s`: Define o tamanho máximo da pilha.
- `-t`: Define o tempo máximo de CPU em segundos.

## Common Examples

Aqui estão alguns exemplos práticos do uso do `ulimit`:

1. **Exibir todos os limites atuais:**

   ```bash
   ulimit -a
   ```

2. **Definir o número máximo de arquivos abertos para 1024:**

   ```bash
   ulimit -n 1024
   ```

3. **Definir o tamanho máximo do arquivo de core dump para 0 (desabilitar):**

   ```bash
   ulimit -c 0
   ```

4. **Definir o tamanho máximo da pilha para 8192 KB:**

   ```bash
   ulimit -s 8192
   ```

5. **Definir o tempo máximo de CPU para 60 segundos:**

   ```bash
   ulimit -t 60
   ```

## Tips
- Sempre verifique os limites atuais com `ulimit -a` antes de fazer alterações, para entender o que está sendo modificado.
- Use `ulimit` em scripts para garantir que os processos não excedam os limites de recursos definidos.
- Lembre-se de que as alterações feitas com `ulimit` são aplicáveis apenas ao shell atual e seus subprocessos; não afetam outros shells ou processos em execução.