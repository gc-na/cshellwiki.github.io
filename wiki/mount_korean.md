# [리눅스] C Shell (csh) mount 사용법: 파일 시스템을 마운트합니다.

## Overview
`mount` 명령은 파일 시스템을 특정 디렉토리에 연결하여 사용자가 해당 파일 시스템의 파일에 접근할 수 있도록 합니다. 이 명령은 주로 외부 저장 장치나 네트워크 파일 시스템을 시스템에 연결할 때 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```
mount [options] [arguments]
```

## Common Options
- `-t type`: 마운트할 파일 시스템의 유형을 지정합니다.
- `-o options`: 마운트 옵션을 설정합니다. 예를 들어, 읽기 전용으로 마운트할 수 있습니다.
- `-a`: `/etc/fstab` 파일에 정의된 모든 파일 시스템을 마운트합니다.
- `-r`: 읽기 전용으로 마운트합니다.

## Common Examples
다음은 `mount` 명령의 몇 가지 일반적인 사용 예입니다.

1. USB 드라이브를 `/mnt/usb`에 마운트하기:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. NFS 파일 시스템을 마운트하기:
   ```bash
   mount -t nfs 192.168.1.100:/exported/path /mnt/nfs
   ```

3. 읽기 전용으로 마운트하기:
   ```bash
   mount -o ro /dev/sdc1 /mnt/readonly
   ```

4. `/etc/fstab`에 정의된 모든 파일 시스템 마운트하기:
   ```bash
   mount -a
   ```

## Tips
- 마운트할 디렉토리가 존재하는지 확인하세요. 존재하지 않는 경우, `mount` 명령이 실패할 수 있습니다.
- 마운트 해제할 때는 `umount` 명령을 사용하세요. 예를 들어, `/mnt/usb`를 해제하려면 `umount /mnt/usb`를 입력합니다.
- 파일 시스템을 마운트할 때는 항상 적절한 권한이 있는지 확인하세요. 일반적으로 `root` 사용자 권한이 필요합니다.