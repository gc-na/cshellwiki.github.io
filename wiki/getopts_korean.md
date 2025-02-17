# [리눅스] Bash getopts 사용법: 옵션 파싱을 위한 유틸리티

## Overview
`getopts`는 Bash 스크립트에서 명령줄 옵션을 파싱하는 데 사용되는 내장 명령어입니다. 이를 통해 스크립트에 전달된 인수들을 쉽게 처리하고, 사용자에게 친숙한 방식으로 옵션을 관리할 수 있습니다.

## Usage
`getopts`의 기본 구문은 다음과 같습니다:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: 옵션을 처리할 때 사용할 수 있는 추가 옵션을 지정합니다.
- `-n`: 스크립트의 이름을 설정합니다.
- `-o`: 단일 문자 옵션을 정의합니다.

## Common Examples

### 예제 1: 기본 옵션 파싱
아래의 스크립트는 `-a`와 `-b` 옵션을 처리합니다.

```bash
#!/bin/bash

while getopts "ab" opt; do
  case $opt in
    a)
      echo "옵션 A가 선택되었습니다."
      ;;
    b)
      echo "옵션 B가 선택되었습니다."
      ;;
    *)
      echo "유효하지 않은 옵션입니다."
      ;;
  esac
done
```

### 예제 2: 인수와 함께 옵션 사용
다음 스크립트는 옵션과 함께 인수를 처리합니다.

```bash
#!/bin/bash

while getopts "f:n:" opt; do
  case $opt in
    f)
      echo "파일: $OPTARG"
      ;;
    n)
      echo "이름: $OPTARG"
      ;;
    *)
      echo "유효하지 않은 옵션입니다."
      ;;
  esac
done
```

### 예제 3: 기본값 설정
옵션이 제공되지 않았을 때 기본값을 설정하는 방법입니다.

```bash
#!/bin/bash

name="기본이름"

while getopts "n:" opt; do
  case $opt in
    n)
      name=$OPTARG
      ;;
    *)
      echo "유효하지 않은 옵션입니다."
      ;;
  esac
done

echo "안녕하세요, $name!"
```

## Tips
- 스크립트에서 `getopts`를 사용할 때, 옵션 문자를 명확하게 정의하여 사용자에게 친숙한 경험을 제공하세요.
- `OPTARG` 변수를 사용하여 옵션에 대한 인수를 쉽게 참조할 수 있습니다.
- 오류 처리를 위해 `*)` 케이스를 추가하여 유효하지 않은 옵션에 대한 피드백을 제공하는 것이 좋습니다.