# [리눅스] Bash hostnamectl 사용법: 시스템 호스트네임 관리

## Overview
`hostnamectl` 명령어는 시스템의 호스트네임을 관리하고, 관련된 정보를 조회하는 데 사용됩니다. 이 명령어를 통해 현재 호스트네임을 확인하거나 변경할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: 새로운 호스트네임을 설정합니다.
- `status`: 현재 호스트네임 및 관련 정보를 표시합니다.
- `set-icon-name`: 아이콘 이름을 설정합니다.
- `set-chassis`: 시스템의 섀시 유형을 설정합니다.

## Common Examples
- 현재 호스트네임 확인하기:
```bash
hostnamectl status
```

- 호스트네임 변경하기:
```bash
sudo hostnamectl set-hostname new-hostname
```

- 시스템의 섀시 유형 설정하기:
```bash
sudo hostnamectl set-chassis laptop
```

- 아이콘 이름 설정하기:
```bash
sudo hostnamectl set-icon-name computer-laptop
```

## Tips
- 호스트네임을 변경한 후에는 시스템을 재부팅할 필요가 없지만, 일부 서비스는 재시작이 필요할 수 있습니다.
- 호스트네임은 알파벳, 숫자, 하이픈(-)만 포함할 수 있으며, 공백은 사용할 수 없습니다.
- 변경 후 `hostnamectl status` 명령어로 변경 사항을 확인하는 것이 좋습니다.