# [Linux] Bash mount uso: Montar sistemas de arquivos

## Overview
O comando `mount` é utilizado para montar sistemas de arquivos em diretórios específicos no Linux. Isso permite que o sistema operacional acesse e utilize dados armazenados em dispositivos de armazenamento, como discos rígidos, pen drives e partições.

## Usage
A sintaxe básica do comando `mount` é a seguinte:

```bash
mount [opções] [dispositivo] [ponto_de_montagem]
```

## Common Options
Aqui estão algumas opções comuns do comando `mount`:

- `-t tipo`: Especifica o tipo de sistema de arquivos (por exemplo, ext4, ntfs).
- `-o opções`: Permite passar opções adicionais, como `ro` (somente leitura) ou `rw` (leitura e escrita).
- `-a`: Monta todos os sistemas de arquivos listados no arquivo `/etc/fstab`.
- `-r`: Monta o sistema de arquivos como somente leitura.

## Common Examples

### Montar um sistema de arquivos
Para montar um dispositivo, como um pen drive, em um diretório específico:

```bash
mount /dev/sdb1 /mnt/pendrive
```

### Montar com opções específicas
Para montar um sistema de arquivos NTFS como somente leitura:

```bash
mount -t ntfs -o ro /dev/sdc1 /mnt/ntfs
```

### Montar todos os sistemas de arquivos
Para montar todos os sistemas de arquivos listados no arquivo `/etc/fstab`:

```bash
mount -a
```

### Montar um sistema de arquivos com opções adicionais
Para montar um sistema de arquivos ext4 com leitura e escrita:

```bash
mount -t ext4 -o rw /dev/sda1 /mnt/ext4
```

## Tips
- Sempre verifique se o ponto de montagem está vazio antes de montar um sistema de arquivos para evitar perda de dados.
- Utilize o comando `umount` para desmontar um sistema de arquivos antes de removê-lo fisicamente.
- Consulte o arquivo `/etc/fstab` para verificar as montagens automáticas configuradas para o sistema.