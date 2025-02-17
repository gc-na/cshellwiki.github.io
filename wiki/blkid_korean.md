# [리눅스] Bash blkid 사용법: 블록 장치의 UUID 및 파일 시스템 정보 조회

## Overview
`blkid` 명령어는 리눅스 시스템에서 블록 장치의 UUID, 파일 시스템 유형 및 기타 정보를 조회하는 데 사용됩니다. 이 명령어는 주로 디스크 파티션과 관련된 정보를 확인할 때 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: 출력 형식을 지정합니다. 예를 들어, `value`를 사용하면 값만 출력됩니다.
- `-s, --match-tag`: 특정 태그에 대한 정보를 필터링합니다.
- `-p, --probe`: 장치의 정보를 프로브하여 최신 정보를 가져옵니다.
- `-c, --cache`: 캐시 파일을 사용하여 성능을 향상시킵니다.

## Common Examples
- 모든 블록 장치 정보 조회:
  ```bash
  blkid
  ```

- 특정 장치의 UUID 조회:
  ```bash
  blkid /dev/sda1
  ```

- 출력 형식을 값으로 설정하여 UUID만 출력:
  ```bash
  blkid -o value -s UUID /dev/sda1
  ```

- 특정 파일 시스템 유형의 장치만 조회:
  ```bash
  blkid -t TYPE=ext4
  ```

## Tips
- `blkid` 명령어는 루트 권한이 필요할 수 있으므로, 필요한 경우 `sudo`를 사용하세요.
- 자주 사용하는 옵션을 스크립트에 저장하여 효율성을 높일 수 있습니다.
- 블록 장치의 변경 사항을 반영하려면 `-p` 옵션을 사용하여 정보를 업데이트하세요.