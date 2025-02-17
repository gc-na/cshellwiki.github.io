# [리눅스] Bash rmdir 사용법: 빈 디렉토리 삭제

## Overview
`rmdir` 명령어는 빈 디렉토리를 삭제하는 데 사용됩니다. 이 명령어는 디렉토리가 비어 있을 때만 작동하며, 내용이 있는 디렉토리는 삭제할 수 없습니다.

## Usage
기본 구문은 다음과 같습니다:

```
rmdir [옵션] [인수]
```

## Common Options
- `-p`: 상위 디렉토리도 함께 삭제합니다. 상위 디렉토리가 비어 있을 경우에만 작동합니다.
- `--ignore-fail-on-non-empty`: 비어 있지 않은 디렉토리를 삭제하려고 할 때 오류 메시지를 무시합니다.

## Common Examples
- 빈 디렉토리 삭제하기:
    ```bash
    rmdir my_empty_directory
    ```

- 상위 디렉토리도 함께 삭제하기:
    ```bash
    rmdir -p parent_directory/child_directory
    ```

- 비어 있지 않은 디렉토리에 대한 오류 무시하기:
    ```bash
    rmdir --ignore-fail-on-non-empty my_non_empty_directory
    ```

## Tips
- `rmdir`를 사용하기 전에 디렉토리가 비어 있는지 확인하세요. `ls` 명령어를 사용하여 디렉토리 내용을 확인할 수 있습니다.
- 여러 디렉토리를 한 번에 삭제하려면, 공백으로 구분하여 인수를 나열할 수 있습니다.
- 실수로 중요한 디렉토리를 삭제하지 않도록 주의하세요. `rmdir`는 삭제된 디렉토리를 복구할 수 없습니다.