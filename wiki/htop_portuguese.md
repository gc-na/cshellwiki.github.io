# [Linux] Bash htop Uso: Monitore o uso de recursos do sistema

## Overview
O comando `htop` é uma ferramenta interativa de monitoramento de processos para sistemas Unix-like. Ele fornece uma visão dinâmica e em tempo real do uso de recursos do sistema, como CPU, memória e processos em execução, permitindo que os usuários gerenciem e visualizem informações de forma mais intuitiva em comparação ao comando `top`.

## Usage
A sintaxe básica do comando `htop` é a seguinte:

```bash
htop [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o `htop`:

- `-h`, `--help`: Exibe a ajuda sobre o uso do htop.
- `-s`, `--sort`: Permite especificar a coluna pela qual os processos devem ser ordenados.
- `-p`, `--pid`: Permite monitorar processos específicos, fornecendo seus IDs de processo (PIDs).
- `-C`, `--no-color`: Executa o htop sem cores, útil para terminais que não suportam cores.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `htop`:

1. **Executar htop simples**:
   ```bash
   htop
   ```

2. **Ordenar processos por uso de memória**:
   ```bash
   htop -s MEM%
   ```

3. **Monitorar processos específicos**:
   ```bash
   htop -p 1234,5678
   ```

4. **Executar htop sem cores**:
   ```bash
   htop -C
   ```

## Tips
- Utilize as teclas de função (F1 a F10) para acessar diferentes funcionalidades do htop, como ajuda, busca e configuração.
- Você pode usar as setas do teclado para navegar entre os processos e pressionar `F9` para matar um processo selecionado.
- Ajuste a atualização do htop pressionando `F2` para acessar as configurações e modificar a taxa de atualização conforme necessário.