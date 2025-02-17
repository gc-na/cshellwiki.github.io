# [Linux] Bash tput Uso: Controle de terminal e formatação de texto

## Overview
O comando `tput` é utilizado para controlar a interface do terminal, permitindo que os usuários modifiquem a aparência do texto, como cores e formatação, além de manipular o cursor e outras características do terminal.

## Usage
A sintaxe básica do comando `tput` é a seguinte:

```bash
tput [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `tput`:

- `setaf [número]`: Define a cor do texto (foreground) para o número especificado.
- `setab [número]`: Define a cor do fundo (background) para o número especificado.
- `bold`: Ativa o texto em negrito.
- `smso`: Ativa o modo de destaque (standout mode).
- `rmso`: Desativa o modo de destaque.
- `cup [linha] [coluna]`: Move o cursor para a linha e coluna especificadas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `tput`:

1. **Alterar a cor do texto para vermelho:**
   ```bash
   tput setaf 1
   echo "Este texto é vermelho"
   tput sgr0  # Reseta as configurações
   ```

2. **Alterar a cor de fundo para azul e o texto para branco:**
   ```bash
   tput setab 4
   tput setaf 7
   echo "Texto com fundo azul e texto branco"
   tput sgr0  # Reseta as configurações
   ```

3. **Ativar texto em negrito:**
   ```bash
   tput bold
   echo "Este texto está em negrito"
   tput sgr0  # Reseta as configurações
   ```

4. **Mover o cursor para a linha 5, coluna 10:**
   ```bash
   tput cup 5 10
   echo "Texto na linha 5, coluna 10"
   ```

## Tips
- Sempre use `tput sgr0` após aplicar formatações para garantir que o terminal volte ao estado normal.
- Teste diferentes números para cores, pois eles podem variar dependendo do terminal que você está utilizando.
- Combine várias opções para criar saídas de texto mais atraentes e informativas.