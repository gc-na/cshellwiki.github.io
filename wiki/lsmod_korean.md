# [리눅스] C Shell (csh) lsmod 사용법: 모듈 상태 확인

## Overview
`lsmod` 명령어는 현재 커널에 로드된 모듈의 목록을 표시합니다. 이 명령어를 사용하면 시스템에서 활성화된 드라이버와 모듈을 쉽게 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
lsmod [options] [arguments]
```

## Common Options
- `-h`, `--help`: 도움말 메시지를 표시합니다.
- `-v`, `--verbose`: 자세한 정보를 출력합니다.

## Common Examples
다음은 `lsmod` 명령어의 몇 가지 실용적인 예입니다:

1. 현재 로드된 모든 모듈 목록 보기:
   ```bash
   lsmod
   ```

2. 도움말 메시지 보기:
   ```bash
   lsmod --help
   ```

3. 자세한 정보 출력:
   ```bash
   lsmod --verbose
   ```

## Tips
- `lsmod`의 출력 결과는 모듈 이름, 크기, 사용 중인 카운트 등을 포함하므로, 시스템의 상태를 파악하는 데 유용합니다.
- 모듈을 추가하거나 제거하기 전에 `lsmod`를 사용하여 현재 상태를 확인하는 것이 좋습니다.