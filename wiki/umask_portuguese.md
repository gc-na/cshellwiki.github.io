# [Linux] Bash umask Uso: Define permissões padrão de arquivos e diretórios

## Overview
O comando `umask` é utilizado para definir as permissões padrão de arquivos e diretórios criados em um sistema Unix/Linux. Ele determina quais permissões serão negadas, influenciando assim as permissões finais dos novos arquivos e diretórios.

## Usage
A sintaxe básica do comando `umask` é a seguinte:

```bash
umask [opções] [máscara]
```

## Common Options
- `-S`: Exibe a máscara de permissão em formato simbólico.
- `-p`: Exibe a máscara de permissão atual em um formato que pode ser usado em um script.

## Common Examples

### Exibir a máscara atual
Para ver a máscara de permissão atual, você pode simplesmente usar:

```bash
umask
```

### Definir uma nova máscara
Para definir uma nova máscara que negue permissões de escrita para o grupo e outros, use:

```bash
umask 022
```

### Usar formato simbólico
Para exibir a máscara atual em formato simbólico, utilize:

```bash
umask -S
```

### Definir máscara em formato simbólico
Para definir uma nova máscara de forma simbólica que negue a permissão de escrita para outros, você pode usar:

```bash
umask u=rwx,g=rx,o=rx
```

## Tips
- Sempre verifique a máscara atual antes de criar novos arquivos, para garantir que as permissões estejam configuradas conforme desejado.
- Considere adicionar o comando `umask` em seus arquivos de inicialização, como `.bashrc` ou `.profile`, para definir suas preferências de máscara de forma persistente.
- Use a opção `-S` para entender melhor as permissões em um formato mais legível, especialmente se você estiver começando a trabalhar com permissões no Linux.