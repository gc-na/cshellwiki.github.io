# [Linux] Bash bindkey Uso: Configurar teclas de atalho no shell

## Overview
O comando `bindkey` é utilizado em ambientes de shell, como o Zsh, para configurar e modificar as teclas de atalho. Ele permite que os usuários personalizem a maneira como as teclas interagem com o terminal, facilitando a execução de comandos e a navegação.

## Usage
A sintaxe básica do comando `bindkey` é a seguinte:

```bash
bindkey [opções] [argumentos]
```

## Common Options
- `-L`: Lista todos os mapeamentos de teclas atuais.
- `-e`: Define o modo de edição para Emacs.
- `-v`: Define o modo de edição para Vi.
- `-s`: Permite que uma sequência de teclas seja vinculada a um comando.

## Common Examples

### Listar mapeamentos de teclas
Para listar todos os mapeamentos de teclas atuais, você pode usar:

```bash
bindkey -L
```

### Definir uma tecla de atalho para um comando
Para vincular a tecla `Ctrl + x` ao comando `ls`, você pode usar:

```bash
bindkey '^x' 'ls\n'
```

### Alterar o modo de edição para Emacs
Para mudar o modo de edição para Emacs, utilize:

```bash
bindkey -e
```

### Vincular uma sequência de teclas a um comando
Para vincular a sequência `Alt + t` ao comando `top`, você pode usar:

```bash
bindkey 'M-t' 'top\n'
```

## Tips
- Sempre verifique os mapeamentos de teclas existentes antes de criar novos, para evitar conflitos.
- Use comentários em seu arquivo de configuração para lembrar o propósito de cada atalho.
- Teste suas configurações de `bindkey` em um terminal separado para evitar problemas no terminal principal.