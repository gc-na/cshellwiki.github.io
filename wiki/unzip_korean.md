# [리눅스] Bash unzip 사용법: 압축 해제 명령어

## Overview
`unzip` 명령어는 ZIP 파일 형식으로 압축된 파일을 해제하는 데 사용됩니다. 이 명령어를 통해 사용자는 압축된 파일의 내용을 쉽게 추출할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
unzip [options] [arguments]
```

## Common Options
- `-l`: ZIP 파일의 내용 목록을 표시합니다.
- `-d <directory>`: 압축 해제할 파일을 지정한 디렉토리에 저장합니다.
- `-o`: 기존 파일을 덮어쓰도록 합니다.
- `-q`: 작업 중 출력 메시지를 최소화합니다.

## Common Examples
- ZIP 파일의 내용을 확인하려면:
```bash
unzip -l example.zip
```

- 현재 디렉토리에 ZIP 파일을 압축 해제하려면:
```bash
unzip example.zip
```

- 특정 디렉토리에 압축 해제하려면:
```bash
unzip example.zip -d /path/to/directory
```

- 기존 파일을 덮어쓰고 압축 해제하려면:
```bash
unzip -o example.zip
```

## Tips
- 압축 해제할 디렉토리를 미리 생성해 두면 관리가 용이합니다.
- `-q` 옵션을 사용하여 스크립트에서 실행할 때 불필요한 출력 메시지를 줄일 수 있습니다.
- ZIP 파일이 비밀번호로 보호되어 있는 경우, `unzip` 명령어는 비밀번호 입력을 요구합니다.