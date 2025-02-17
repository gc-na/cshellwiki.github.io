# [리눅스] Bash shutdown 사용법: 시스템 종료 및 재부팅

## Overview
`shutdown` 명령어는 시스템을 안전하게 종료하거나 재부팅하는 데 사용됩니다. 이 명령어는 시스템 관리자에게 서버나 컴퓨터를 종료할 수 있는 방법을 제공합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
shutdown [options] [time] [message]
```

## Common Options
- `-h` 또는 `--halt`: 시스템을 종료합니다.
- `-r` 또는 `--reboot`: 시스템을 재부팅합니다.
- `-c`: 예약된 종료를 취소합니다.
- `time`: 종료 또는 재부팅을 수행할 시간을 지정합니다. 예를 들어, `now`는 즉시 종료를 의미합니다.
- `message`: 사용자에게 전송할 메시지를 지정합니다.

## Common Examples
1. 즉시 시스템 종료:
   ```bash
   shutdown -h now
   ```

2. 1분 후 시스템 재부팅:
   ```bash
   shutdown -r +1
   ```

3. 특정 시간에 시스템 종료 (예: 22:00):
   ```bash
   shutdown -h 22:00
   ```

4. 예약된 종료 취소:
   ```bash
   shutdown -c
   ```

5. 사용자에게 종료 메시지 전송:
   ```bash
   shutdown -h now "시스템이 곧 종료됩니다."
   ```

## Tips
- 시스템 종료 전에 중요한 작업을 저장하는 것을 잊지 마세요.
- 서버를 관리하는 경우, 사용자에게 종료 예정 시간을 미리 알리는 것이 좋습니다.
- `shutdown` 명령어를 사용할 때는 관리자 권한이 필요할 수 있습니다. `sudo`를 사용하여 권한을 부여하세요.