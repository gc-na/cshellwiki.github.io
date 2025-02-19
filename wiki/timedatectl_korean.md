# [리눅스] C Shell (csh) timedatectl 사용법: 시스템 시간 및 날짜 관리

## 개요
`timedatectl` 명령은 시스템의 시간 및 날짜를 설정하고 관리하는 데 사용됩니다. 이 명령은 시스템의 현재 시간, 날짜, 타임존 및 NTP(Network Time Protocol) 설정을 확인하고 조정할 수 있는 기능을 제공합니다.

## 사용법
기본 구문은 다음과 같습니다:
```csh
timedatectl [옵션] [인수]
```

## 일반 옵션
- `status`: 현재 시간, 날짜 및 타임존 정보를 표시합니다.
- `set-time`: 시스템 시간을 설정합니다.
- `set-timezone`: 시스템의 타임존을 설정합니다.
- `set-ntp`: NTP 동기화를 활성화 또는 비활성화합니다.

## 일반 예제
- 현재 시간 및 날짜 확인:
```csh
timedatectl status
```

- 시스템 시간 설정 (예: 2023년 10월 1일 12시 30분):
```csh
timedatectl set-time '2023-10-01 12:30:00'
```

- 타임존 설정 (예: 서울):
```csh
timedatectl set-timezone Asia/Seoul
```

- NTP 동기화 활성화:
```csh
timedatectl set-ntp true
```

## 팁
- 시스템 시간을 변경할 때는 관리자 권한이 필요할 수 있습니다.
- 타임존을 설정할 때는 `timedatectl list-timezones` 명령을 사용하여 사용 가능한 타임존 목록을 확인할 수 있습니다.
- NTP 동기화를 활성화하면 시스템 시간이 자동으로 인터넷 시간 서버와 동기화됩니다.