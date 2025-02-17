# [Linux] Bash cd Uso: Mudar de diretório

## Overview
O comando `cd` (change directory) é utilizado no Bash para mudar o diretório de trabalho atual. Isso permite que você navegue entre diferentes pastas no sistema de arquivos.

## Usage
A sintaxe básica do comando `cd` é a seguinte:

```bash
cd [opções] [argumentos]
```

## Common Options
O comando `cd` possui algumas opções comuns que podem ser úteis:

- `-`: Retorna ao diretório anterior.
- `..`: Move para o diretório pai do diretório atual.
- `~`: Leva você ao diretório home do usuário atual.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cd`:

1. Mudar para um diretório específico:
   ```bash
   cd /caminho/para/o/diretorio
   ```

2. Voltar ao diretório anterior:
   ```bash
   cd -
   ```

3. Subir um nível na hierarquia de diretórios:
   ```bash
   cd ..
   ```

4. Ir para o diretório home do usuário:
   ```bash
   cd ~
   ```

5. Mudar para um diretório relativo:
   ```bash
   cd pasta/subpasta
   ```

## Tips
- Utilize `cd -` para alternar rapidamente entre dois diretórios.
- Use `cd ..` várias vezes para subir vários níveis na árvore de diretórios.
- O uso de caminhos relativos pode economizar tempo ao navegar em diretórios próximos.