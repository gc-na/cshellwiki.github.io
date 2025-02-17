# [리눅스] Bash sed 사용법: 텍스트 변환 및 편집

## Overview
`sed`는 스트림 편집기(Stream Editor)로, 텍스트 파일의 내용을 수정하거나 변환하는 데 사용됩니다. 주로 파일의 특정 부분을 찾고, 대체하거나 삭제하는 작업에 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 여러 개의 편집 명령을 지정할 때 사용합니다.
- `-i`: 파일을 직접 수정합니다. 백업 파일을 만들고 싶다면 `-i.bak`와 같이 사용할 수 있습니다.
- `-n`: 기본적으로 출력하지 않으며, 명시적으로 출력할 때만 결과를 보여줍니다.

## Common Examples
- **문자열 대체**: 파일 내에서 특정 문자열을 다른 문자열로 대체합니다.
    ```bash
    sed 's/old_string/new_string/g' filename.txt
    ```

- **행 삭제**: 특정 패턴이 포함된 행을 삭제합니다.
    ```bash
    sed '/pattern/d' filename.txt
    ```

- **행 번호 지정**: 특정 행 번호를 출력합니다.
    ```bash
    sed -n '3p' filename.txt
    ```

- **파일 직접 수정**: 파일 내의 문자열을 직접 수정합니다.
    ```bash
    sed -i 's/old_string/new_string/g' filename.txt
    ```

## Tips
- `sed` 명령어를 사용할 때는 정규 표현식을 활용하면 더욱 강력한 텍스트 처리가 가능합니다.
- 대체 작업을 수행할 때는 `g` 플래그를 사용하여 해당 행의 모든 인스턴스를 변경할 수 있습니다.
- 파일을 수정하기 전에 항상 백업을 만들어 두는 것이 좋습니다. `-i.bak` 옵션을 사용하면 원본 파일의 백업을 자동으로 생성할 수 있습니다.