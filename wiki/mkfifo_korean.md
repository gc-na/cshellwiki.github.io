# [리눅스] C Shell (csh) mkfifo 사용법: FIFO(선입선출) 파일 생성

## Overview
`mkfifo` 명령은 FIFO(선입선출) 특성을 가진 파일을 생성하는 데 사용됩니다. FIFO 파일은 프로세스 간에 데이터를 전송하는 데 유용하며, 한 프로세스가 데이터를 쓰면 다른 프로세스가 이를 읽을 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE`: 새로 생성할 FIFO 파일의 권한 모드를 설정합니다.
- `--help`: `mkfifo` 명령에 대한 도움말을 표시합니다.
- `--version`: `mkfifo` 명령의 버전 정보를 표시합니다.

## Common Examples
다음은 `mkfifo` 명령의 몇 가지 일반적인 예입니다.

1. 기본 FIFO 파일 생성:
   ```csh
   mkfifo myfifo
   ```

2. 특정 권한 모드로 FIFO 파일 생성:
   ```csh
   mkfifo -m 644 myfifo
   ```

3. 여러 FIFO 파일을 한 번에 생성:
   ```csh
   mkfifo fifo1 fifo2 fifo3
   ```

## Tips
- FIFO 파일은 프로세스 간의 통신을 위해 사용되므로, 생성 후에는 반드시 데이터를 읽고 쓸 프로세스를 준비해야 합니다.
- FIFO 파일을 삭제하려면 `rm` 명령을 사용하십시오.
- FIFO 파일의 권한을 적절히 설정하여 보안을 유지하는 것이 중요합니다.