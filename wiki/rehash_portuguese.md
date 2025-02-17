# [Linux] Bash rehash uso: Atualiza o cache de comandos

## Overview
O comando `rehash` é utilizado em ambientes de shell, como o Bash, para atualizar o cache de comandos disponíveis. Isso é especialmente útil quando novos executáveis são adicionados a diretórios que já estão no PATH, permitindo que o shell reconheça esses novos comandos sem a necessidade de reiniciar a sessão.

## Usage
A sintaxe básica do comando `rehash` é a seguinte:

```bash
rehash [options] [arguments]
```

## Common Options
O comando `rehash` não possui muitas opções, mas aqui estão algumas que podem ser relevantes:

- **-p**: Atualiza apenas o cache de comandos para o diretório atual.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `rehash`:

1. **Atualizar o cache de comandos após instalar um novo programa**:
   ```bash
   rehash
   ```

2. **Atualizar o cache apenas para o diretório atual**:
   ```bash
   rehash -p
   ```

## Tips
- Sempre que você instalar um novo software ou adicionar um novo executável a um diretório que já está no seu PATH, é uma boa prática executar `rehash` para garantir que o shell reconheça o novo comando.
- Se você estiver usando um shell que não suporta `rehash`, considere reiniciar a sessão do terminal ou usar o comando `hash -r` para limpar o cache de comandos.
- O comando `rehash` é mais comum em shells como o `tcsh` e `csh`, enquanto no Bash, a necessidade de usá-lo é menos frequente, pois o Bash atualiza automaticamente o cache de comandos.