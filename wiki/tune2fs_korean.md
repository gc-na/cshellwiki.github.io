# [리눅스] Bash tune2fs 사용법: 파일 시스템 파라미터 조정

## Overview
`tune2fs` 명령어는 ext2, ext3, ext4 파일 시스템의 파라미터를 조정하는 데 사용됩니다. 이 명령어를 통해 파일 시스템의 성능과 기능을 최적화할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tune2fs [옵션] [인수]
```

## Common Options
- `-c <num>`: 파일 시스템의 최대 마운트 횟수를 설정합니다.
- `-i <interval>`: 파일 시스템의 점검 주기를 설정합니다.
- `-m <percentage>`: 예약된 블록의 비율을 설정합니다.
- `-o <options>`: 파일 시스템의 마운트 옵션을 설정합니다.
- `-L <label>`: 파일 시스템의 레이블을 변경합니다.

## Common Examples
- 최대 마운트 횟수를 20으로 설정:
```bash
tune2fs -c 20 /dev/sda1
```

- 점검 주기를 30일로 설정:
```bash
tune2fs -i 30d /dev/sda1
```

- 예약된 블록 비율을 5%로 설정:
```bash
tune2fs -m 5 /dev/sda1
```

- 파일 시스템의 레이블을 "MyDisk"로 변경:
```bash
tune2fs -L MyDisk /dev/sda1
```

## Tips
- `tune2fs`를 사용하기 전에 파일 시스템이 마운트 해제되어 있는지 확인하세요.
- 변경 사항을 적용하기 전에 현재 설정을 백업해 두는 것이 좋습니다.
- 파일 시스템의 상태를 확인하려면 `tune2fs -l /dev/sda1` 명령어를 사용하여 현재 파라미터를 확인할 수 있습니다.