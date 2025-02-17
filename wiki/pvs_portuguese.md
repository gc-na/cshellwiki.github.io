# [Linux] Bash pvs Uso equivalente: Exibir informações sobre volumes lógicos

## Overview
O comando `pvs` é utilizado para exibir informações sobre os volumes físicos em um sistema Linux que utiliza o gerenciamento de volumes lógicos (LVM). Ele fornece uma visão geral dos volumes físicos, incluindo detalhes como tamanho, espaço utilizado e atributos.

## Usage
A sintaxe básica do comando `pvs` é a seguinte:

```bash
pvs [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `pvs`:

- `-o, --options`: Especifica quais informações exibir.
- `-u, --units`: Exibe tamanhos em unidades legíveis (por exemplo, MB, GB).
- `-f, --noheadings`: Remove os cabeçalhos da saída.
- `-d, --debug`: Ativa a saída de depuração para ajudar na resolução de problemas.

## Common Examples

### Exibir todos os volumes físicos
Para listar todos os volumes físicos no sistema, você pode usar o seguinte comando:

```bash
pvs
```

### Exibir informações detalhadas
Para obter informações mais detalhadas sobre os volumes físicos, use a opção `-o`:

```bash
pvs -o +pv_size,pv_free
```

### Exibir tamanhos em unidades legíveis
Para mostrar os tamanhos em unidades mais compreensíveis, utilize a opção `-u`:

```bash
pvs -u
```

### Remover cabeçalhos da saída
Se você deseja uma saída mais limpa, sem cabeçalhos, use a opção `-f`:

```bash
pvs -f
```

## Tips
- Sempre verifique se você tem permissões adequadas para acessar informações de volumes físicos.
- Combine `pvs` com outros comandos LVM, como `lvdisplay` e `vgdisplay`, para obter uma visão mais completa do gerenciamento de volumes.
- Utilize a opção `-d` se você encontrar problemas, pois isso pode ajudar a identificar o que está acontecendo.