# [리눅스] Bash vipw 사용법: 사용자 비밀번호 파일 편집

## Overview
`vipw` 명령어는 시스템의 사용자 비밀번호 파일인 `/etc/passwd`와 `/etc/shadow`를 안전하게 편집할 수 있도록 도와주는 도구입니다. 이 명령어는 파일을 잠그고, 편집이 완료되면 자동으로 변경 사항을 적용하여 데이터 손상을 방지합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
vipw [options]
```

## Common Options
- `-s`: `/etc/shadow` 파일을 편집합니다.
- `-f <file>`: 지정한 파일을 편집합니다. 기본적으로 `/etc/passwd`를 편집합니다.

## Common Examples
1. 기본적으로 사용자 비밀번호 파일을 편집하기:
   ```bash
   vipw
   ```

2. `/etc/shadow` 파일을 편집하기:
   ```bash
   vipw -s
   ```

3. 특정 파일을 편집하기 (예: `/etc/passwd`):
   ```bash
   vipw -f /etc/passwd
   ```

## Tips
- `vipw`를 사용할 때는 항상 주의하여 편집하세요. 잘못된 변경은 시스템에 문제를 일으킬 수 있습니다.
- 변경 후에는 항상 파일을 저장하고 종료하여 변경 사항이 적용되도록 하세요.
- 시스템의 보안을 위해 `vipw`를 사용할 때는 관리자 권한이 필요합니다.