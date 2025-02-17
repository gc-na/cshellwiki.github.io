# [Linux] Bash 7z Uso: Compactar e descompactar arquivos

## Overview
O comando `7z` é uma ferramenta poderosa para compactar e descompactar arquivos, suportando vários formatos de compressão, como 7z, ZIP, RAR, entre outros. Ele é parte do pacote de software p7zip e é amplamente utilizado por sua eficiência e flexibilidade.

## Usage
A sintaxe básica do comando `7z` é a seguinte:

```bash
7z [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `7z`:

- `a`: Adiciona arquivos a um arquivo compactado.
- `x`: Extrai arquivos de um arquivo compactado.
- `l`: Lista o conteúdo de um arquivo compactado.
- `d`: Remove arquivos de um arquivo compactado.
- `t`: Testa a integridade de um arquivo compactado.

## Common Examples

### Compactar arquivos
Para compactar arquivos em um arquivo 7z:

```bash
7z a arquivo.7z arquivo1.txt arquivo2.txt
```

### Descompactar arquivos
Para descompactar um arquivo 7z:

```bash
7z x arquivo.7z
```

### Listar o conteúdo de um arquivo compactado
Para listar os arquivos dentro de um arquivo 7z:

```bash
7z l arquivo.7z
```

### Remover arquivos de um arquivo compactado
Para remover um arquivo específico de um arquivo 7z:

```bash
7z d arquivo.7z arquivo1.txt
```

### Testar a integridade de um arquivo compactado
Para verificar se um arquivo 7z está íntegro:

```bash
7z t arquivo.7z
```

## Tips
- Sempre verifique a integridade dos arquivos compactados usando a opção `t` após a compressão.
- Utilize a opção `-p` para proteger seus arquivos com senha ao compactar.
- Para compactar diretórios inteiros, basta especificar o diretório em vez de arquivos individuais.