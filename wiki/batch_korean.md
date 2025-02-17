# [리눅스] Bash batch 사용법: 작업을 예약하여 실행하기

## Overview
`batch` 명령어는 시스템의 부하가 적은 시간에 작업을 예약하여 실행하는 데 사용됩니다. 사용자가 입력한 명령어를 시스템의 작업 큐에 추가하고, 시스템이 여유가 있을 때 자동으로 실행합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
batch [options] [arguments]
```

## Common Options
- `-f`, `--file`: 명령어가 포함된 파일을 지정합니다.
- `-l`, `--login`: 로그인 셸을 사용하여 명령어를 실행합니다.
- `-q`, `--quiet`: 출력 메시지를 최소화합니다.

## Common Examples
1. **간단한 명령어 예약하기**
   ```bash
   echo "echo Hello World" | batch
   ```
   위 명령어는 시스템이 여유가 있을 때 "Hello World"라는 메시지를 출력합니다.

2. **파일에서 명령어 읽기**
   ```bash
   batch < my_commands.txt
   ```
   `my_commands.txt` 파일에 있는 모든 명령어를 예약하여 실행합니다.

3. **특정 시간에 작업 예약하기**
   ```bash
   echo "python my_script.py" | batch
   ```
   `my_script.py`를 시스템이 여유가 있을 때 실행하도록 예약합니다.

## Tips
- `batch` 명령어는 시스템의 부하가 적은 시간에 실행되므로, 긴 작업을 예약할 때 유용합니다.
- 예약된 작업의 상태를 확인하려면 `atq` 명령어를 사용할 수 있습니다.
- 작업이 완료된 후 결과를 이메일로 받을 수 있도록 설정할 수 있습니다.