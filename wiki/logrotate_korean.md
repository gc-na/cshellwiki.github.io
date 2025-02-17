# [리눅스] Bash logrotate 사용법: 로그 파일 관리

## Overview
logrotate 명령어는 시스템에서 생성되는 로그 파일을 관리하고 회전시키는 데 사용됩니다. 이 명령어는 로그 파일의 크기를 제한하고, 오래된 로그 파일을 삭제하거나 압축하여 디스크 공간을 절약하는 데 도움을 줍니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
logrotate [options] [arguments]
```

## Common Options
- `-f`: 강제로 로그 회전을 수행합니다.
- `-s`: 상태 파일을 지정합니다. 이 파일은 로그 회전 상태를 기록합니다.
- `-v`: 자세한 출력을 표시합니다.
- `-d`: 실제로 회전하지 않고 어떤 일이 일어날지를 시뮬레이션합니다.

## Common Examples
- 기본 로그 회전 실행:
```bash
logrotate /etc/logrotate.conf
```

- 강제로 로그 회전 수행:
```bash
logrotate -f /etc/logrotate.conf
```

- 로그 회전 상태 확인:
```bash
logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
```

- 로그 회전 시뮬레이션:
```bash
logrotate -d /etc/logrotate.conf
```

## Tips
- 로그 회전 설정 파일을 주기적으로 검토하여 필요에 따라 조정하세요.
- 로그 파일의 크기와 보존 기간을 적절히 설정하여 디스크 공간을 효율적으로 사용하세요.
- 로그 회전 후 이메일 알림을 설정하여 시스템 관리자에게 중요한 로그 회전 이벤트를 통지할 수 있습니다.