# [리눅스] Bash 파일 사용법: 파일 유형 확인

## Overview
`file` 명령어는 주어진 파일의 유형을 식별하는 데 사용됩니다. 이 명령어는 파일의 내용과 메타데이터를 분석하여 텍스트 파일, 이미지 파일, 실행 파일 등 다양한 파일 형식을 구분합니다.

## Usage
기본 구문은 다음과 같습니다:
```
file [옵션] [파일 경로]
```

## Common Options
- `-b`: 파일 유형을 간단하게 출력합니다.
- `-i`: MIME 타입을 출력합니다.
- `-f`: 파일 목록을 포함하는 파일을 사용하여 여러 파일의 유형을 확인합니다.

## Common Examples
- 단일 파일의 유형 확인:
```bash
file example.txt
```

- 여러 파일의 유형 확인:
```bash
file example.txt image.png script.sh
```

- MIME 타입 확인:
```bash
file -i example.txt
```

- 파일 목록을 사용하여 유형 확인:
```bash
file -f file_list.txt
```

## Tips
- `file` 명령어는 파일의 내용을 분석하므로, 파일이 손상되었거나 비정상적인 경우에도 유용한 정보를 제공할 수 있습니다.
- 스크립트에서 파일 유형을 확인할 때 `file` 명령어를 사용하여 조건문을 작성하면 유용합니다.