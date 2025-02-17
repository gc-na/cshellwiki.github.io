# [리눅스] Bash exec 사용법: 프로세스 대체 실행

## Overview
`exec` 명령어는 현재 셸 프로세스를 새로운 프로그램으로 대체하는 데 사용됩니다. 이 명령어를 사용하면 새로운 프로세스를 시작하되, 기존의 셸 프로세스는 종료됩니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
exec [options] [arguments]
```

## Common Options
- `-a`: 새로운 프로그램의 이름을 지정합니다.
- `-l`: 로그인 셸로 실행합니다.
- `-c`: 환경 변수를 초기화합니다.

## Common Examples
1. 현재 셸을 `bash`로 대체하기:
   ```bash
   exec bash
   ```

2. 특정 프로그램을 실행하고 기존 셸 종료하기:
   ```bash
   exec /usr/bin/python3
   ```

3. 프로그램 이름을 변경하여 실행하기:
   ```bash
   exec -a newname /path/to/program
   ```

4. 로그인 셸로 `sh` 실행하기:
   ```bash
   exec -l sh
   ```

## Tips
- `exec`를 사용하면 기존 셸이 종료되므로, 중요한 작업을 수행 중이라면 주의해야 합니다.
- 스크립트의 마지막에 `exec`를 사용하여 스크립트가 끝난 후 다른 프로그램으로 전환할 수 있습니다.
- `exec`를 사용하여 리소스를 절약할 수 있으며, 불필요한 프로세스 생성을 피할 수 있습니다.