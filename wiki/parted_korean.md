# [리눅스] Bash parted 사용법: 파티션 관리 도구

## Overview
`parted` 명령어는 리눅스 시스템에서 디스크 파티션을 관리하는 데 사용됩니다. 이 도구를 통해 파티션을 생성, 삭제, 크기 조정 및 파일 시스템을 변경할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
parted [options] [arguments]
```

## Common Options
- `-l`, `--list`: 시스템의 모든 디스크와 파티션 목록을 표시합니다.
- `-s`, `--script`: 대화형 모드를 비활성화하여 스크립트에서 사용할 수 있도록 합니다.
- `mkpart`: 새로운 파티션을 생성합니다.
- `rm`: 기존 파티션을 삭제합니다.
- `resizepart`: 기존 파티션의 크기를 조정합니다.

## Common Examples
1. **디스크 목록 보기**
   ```bash
   parted -l
   ```

2. **새로운 파티션 생성**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **파티션 삭제**
   ```bash
   parted /dev/sda rm 1
   ```

4. **파티션 크기 조정**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

## Tips
- `parted`를 사용할 때는 항상 중요한 데이터의 백업을 먼저 수행하세요.
- `--script` 옵션을 사용하여 자동화된 스크립트에서 `parted`를 실행할 수 있습니다.
- 파티션 작업 후에는 `resize2fs`와 같은 도구를 사용하여 파일 시스템을 조정하는 것을 잊지 마세요.