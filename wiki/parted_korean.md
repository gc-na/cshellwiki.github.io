# [리눅스] C Shell (csh) parted 사용법: 파티션 관리 도구

## Overview
`parted` 명령어는 디스크의 파티션을 관리하는 데 사용됩니다. 이 도구를 통해 파티션을 생성, 삭제, 크기 조정 및 포맷할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
parted [options] [arguments]
```

## Common Options
- `-l`: 현재 시스템의 모든 디스크와 파티션 목록을 표시합니다.
- `-s`: 간단 모드로 실행하여 출력 메시지를 최소화합니다.
- `mkpart`: 새로운 파티션을 생성합니다.
- `rm`: 지정한 파티션을 삭제합니다.
- `resizepart`: 기존 파티션의 크기를 조정합니다.

## Common Examples
- 현재 시스템의 모든 파티션 목록 보기:
  ```bash
  parted -l
  ```

- 새로운 파티션 생성하기 (예: 1GB 크기의 ext4 파티션):
  ```bash
  parted /dev/sda mkpart primary ext4 1GB 2GB
  ```

- 특정 파티션 삭제하기 (예: 1번 파티션):
  ```bash
  parted /dev/sda rm 1
  ```

- 기존 파티션 크기 조정하기 (예: 2번 파티션을 3GB로 조정):
  ```bash
  parted /dev/sda resizepart 2 3GB
  ```

## Tips
- 파티션을 조정하기 전에 항상 중요한 데이터를 백업하세요.
- `parted` 명령어를 사용할 때는 루트 권한이 필요할 수 있습니다.
- 파티션 작업 후에는 파일 시스템을 체크하는 것이 좋습니다.