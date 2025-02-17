# [리눅스] Bash trap 사용법: 신호를 처리하는 방법

## Overview
`trap` 명령은 Bash 스크립트에서 특정 신호를 수신했을 때 실행할 명령을 지정하는 데 사용됩니다. 이를 통해 스크립트가 종료되거나 중단될 때 필요한 정리 작업을 수행할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
trap [options] [commands] [signals]
```

## Common Options
- `-l`: 사용 가능한 신호 목록을 표시합니다.
- `-p`: 현재 설정된 trap을 출력합니다.
- `-n`: 신호를 무시합니다.

## Common Examples
1. **SIGINT 신호 처리하기**
   ```bash
   trap 'echo "프로그램이 종료되었습니다."' SIGINT
   while true; do
       sleep 1
   done
   ```

2. **종료 시 정리 작업 수행하기**
   ```bash
   trap 'rm -f /tmp/tempfile; echo "정리 완료."' EXIT
   touch /tmp/tempfile
   ```

3. **특정 신호 무시하기**
   ```bash
   trap - SIGTERM
   echo "SIGTERM 신호를 무시합니다."
   ```

4. **여러 신호에 대해 동일한 명령 실행하기**
   ```bash
   trap 'echo "종료 신호 수신!"' SIGINT SIGTERM
   while true; do
       sleep 1
   done
   ```

## Tips
- 스크립트의 시작 부분에 trap을 설정하여 모든 신호에 대해 일관된 처리를 할 수 있습니다.
- 여러 신호에 대해 동일한 명령을 실행하려면 신호를 공백으로 구분하여 나열하세요.
- `EXIT` 신호를 사용하면 스크립트가 종료될 때 항상 정리 작업을 수행할 수 있습니다.