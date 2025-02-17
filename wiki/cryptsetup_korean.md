# [리눅스] Bash cryptsetup 사용법: 디스크 암호화 관리

## Overview
`cryptsetup` 명령어는 리눅스에서 디스크 암호화를 관리하는 도구입니다. 이 명령어를 사용하면 LUKS(Linux Unified Key Setup)와 같은 암호화 표준을 통해 블록 디바이스를 암호화하고, 이를 안전하게 마운트할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
cryptsetup [options] [arguments]
```

## Common Options
- `luksFormat`: 디스크를 LUKS 형식으로 초기화합니다.
- `luksOpen`: 암호화된 디스크를 열어 접근할 수 있게 합니다.
- `luksClose`: 열린 LUKS 디스크를 닫습니다.
- `status`: 암호화된 디스크의 상태를 확인합니다.
- `luksAddKey`: LUKS 디스크에 새로운 키를 추가합니다.

## Common Examples
- **디스크 초기화 (LUKS 형식으로)**:
  ```bash
  cryptsetup luksFormat /dev/sdX
  ```

- **암호화된 디스크 열기**:
  ```bash
  cryptsetup luksOpen /dev/sdX my_encrypted_disk
  ```

- **암호화된 디스크 닫기**:
  ```bash
  cryptsetup luksClose my_encrypted_disk
  ```

- **암호화된 디스크 상태 확인**:
  ```bash
  cryptsetup status my_encrypted_disk
  ```

- **새로운 키 추가**:
  ```bash
  cryptsetup luksAddKey /dev/sdX
  ```

## Tips
- 암호화된 디스크를 사용할 때는 항상 안전한 비밀번호를 설정하고, 이를 안전한 장소에 보관하세요.
- 중요한 데이터는 항상 백업해 두는 것이 좋습니다. 암호화된 디스크의 비밀번호를 잊어버리면 데이터 복구가 불가능할 수 있습니다.
- `cryptsetup` 명령어를 사용할 때는 루트 권한이 필요하므로, `sudo`를 사용하여 실행하세요.