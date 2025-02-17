# [리눅스] Bash mount 사용법: 파일 시스템을 마운트합니다.

## Overview
`mount` 명령은 리눅스 및 유닉스 시스템에서 파일 시스템을 특정 디렉토리에 연결하여 사용할 수 있도록 하는 명령입니다. 이를 통해 외부 저장 장치나 다른 파일 시스템의 데이터를 접근할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
mount [options] [arguments]
```

## Common Options
- `-t <type>`: 마운트할 파일 시스템의 유형을 지정합니다. 예: `ext4`, `ntfs`, `vfat` 등.
- `-o <options>`: 마운트 옵션을 추가로 지정합니다. 예: `ro` (읽기 전용), `rw` (읽기/쓰기).
- `-a`: `/etc/fstab` 파일에 정의된 모든 파일 시스템을 마운트합니다.
- `-r`: 파일 시스템을 읽기 전용으로 마운트합니다.

## Common Examples
1. **기본 마운트**
   ```bash
   mount /dev/sdb1 /mnt/mydrive
   ```
   `/dev/sdb1` 장치를 `/mnt/mydrive` 디렉토리에 마운트합니다.

2. **특정 파일 시스템 유형 지정**
   ```bash
   mount -t ext4 /dev/sdb1 /mnt/mydrive
   ```
   `ext4` 파일 시스템으로 `/dev/sdb1`을 마운트합니다.

3. **읽기 전용으로 마운트**
   ```bash
   mount -o ro /dev/sdb1 /mnt/mydrive
   ```
   `/dev/sdb1`을 읽기 전용으로 마운트합니다.

4. **모든 파일 시스템 마운트**
   ```bash
   mount -a
   ```
   `/etc/fstab`에 정의된 모든 파일 시스템을 마운트합니다.

## Tips
- 마운트하기 전에 대상 디렉토리가 존재하는지 확인하세요. 존재하지 않으면 오류가 발생합니다.
- 마운트 해제는 `umount` 명령을 사용하여 수행할 수 있습니다.
- 파일 시스템의 무결성을 유지하기 위해 마운트 해제 전에 모든 파일 작업을 완료하세요.