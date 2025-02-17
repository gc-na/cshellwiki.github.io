# [Linux] Bash killall Uso: Finaliza processos pelo nome

## Overview
O comando `killall` é utilizado para finalizar processos em execução com base no nome do processo. Isso é útil quando você deseja encerrar todos os processos que correspondem a um nome específico sem precisar descobrir seus IDs de processo (PIDs).

## Usage
A sintaxe básica do comando `killall` é a seguinte:

```bash
killall [opções] [nome_do_processo]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `killall`:

- `-u [usuário]`: Finaliza apenas os processos pertencentes ao usuário especificado.
- `-i`: Solicita confirmação antes de finalizar cada processo.
- `-q`: Executa o comando em modo silencioso, sem mensagens de erro.
- `-s [sinal]`: Especifica o sinal a ser enviado ao processo (por padrão, é o sinal TERM).

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `killall`:

1. **Finalizar todos os processos do Firefox:**
   ```bash
   killall firefox
   ```

2. **Finalizar todos os processos do usuário "joão":**
   ```bash
   killall -u joão
   ```

3. **Finalizar todos os processos do Apache com confirmação:**
   ```bash
   killall -i apache2
   ```

4. **Enviar um sinal específico (como SIGKILL) para todos os processos do nome "myapp":**
   ```bash
   killall -s SIGKILL myapp
   ```

5. **Executar o comando em modo silencioso:**
   ```bash
   killall -q myprocess
   ```

## Tips
- Sempre tenha cuidado ao usar `killall`, pois ele pode encerrar múltiplos processos de uma só vez. Verifique o nome do processo antes de executar.
- Utilize a opção `-i` se você não tiver certeza sobre quais processos serão finalizados, pois isso pode evitar encerramentos acidentais.
- Combine `killall` com outros comandos, como `ps`, para listar processos antes de decidir quais encerrar.