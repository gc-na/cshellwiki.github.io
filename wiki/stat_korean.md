# [리눅스] C Shell (csh) stat 사용법: 파일 상태 정보 확인

## Overview
`stat` 명령어는 파일이나 디렉토리에 대한 상세한 상태 정보를 제공합니다. 이 명령어를 사용하면 파일의 크기, 수정 시간, 접근 권한 등 다양한 메타데이터를 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```csh
stat [options] [arguments]
```

## Common Options
- `-c` : 사용자 정의 형식으로 출력합니다.
- `-f` : 파일 시스템 정보를 출력합니다.
- `-L` : 심볼릭 링크를 따라가서 링크가 가리키는 파일의 정보를 표시합니다.

## Common Examples
- 기본 파일 정보 확인:
```csh
stat filename.txt
```

- 사용자 정의 형식으로 출력:
```csh
stat -c '%s bytes, %y' filename.txt
```

- 심볼릭 링크의 정보 확인:
```csh
stat -L symlink
```

- 파일 시스템 정보 확인:
```csh
stat -f filename.txt
```

## Tips
- `stat` 명령어는 파일의 상태를 빠르게 확인할 수 있는 유용한 도구입니다. 자주 사용하는 파일의 메타데이터를 확인할 때 유용합니다.
- 스크립트에서 파일의 수정 시간을 체크할 때 `stat`을 활용하면 자동화 작업에 큰 도움이 됩니다.