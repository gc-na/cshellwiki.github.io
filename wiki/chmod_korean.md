# [리눅스] Bash chmod 사용법: 파일 및 디렉토리 권한 변경

## Overview
`chmod` 명령어는 파일이나 디렉토리의 접근 권한을 변경하는 데 사용됩니다. 이 명령어를 통해 사용자, 그룹 및 기타 사용자에 대한 읽기, 쓰기 및 실행 권한을 설정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
chmod [options] [arguments]
```

## Common Options
- `-R`: 하위 디렉토리 및 파일에 대해 재귀적으로 권한을 변경합니다.
- `-v`: 변경된 권한을 자세히 출력합니다.
- `-c`: 권한이 변경된 경우에만 변경 내용을 출력합니다.
- `--reference=FILE`: 특정 파일의 권한을 참조하여 변경합니다.

## Common Examples
- 파일에 읽기 및 쓰기 권한 부여:
  ```bash
  chmod u+rw filename.txt
  ```

- 모든 사용자에게 실행 권한 부여:
  ```bash
  chmod a+x script.sh
  ```

- 디렉토리와 그 하위 파일에 대해 읽기 및 실행 권한 부여 (재귀적):
  ```bash
  chmod -R a+rx directory_name
  ```

- 특정 파일의 권한을 다른 파일과 동일하게 설정:
  ```bash
  chmod --reference=reference_file.txt target_file.txt
  ```

## Tips
- 권한 변경 후 `ls -l` 명령어를 사용하여 변경 사항을 확인하세요.
- 권한을 설정할 때는 항상 최소 권한 원칙을 따르세요. 필요한 권한만 부여하는 것이 좋습니다.
- 스크립트 파일에는 실행 권한을 부여하여 쉽게 실행할 수 있도록 하세요.