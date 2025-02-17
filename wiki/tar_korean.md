# [리눅스] Bash tar 사용법: 파일 아카이브 및 압축

## Overview
`tar` 명령어는 파일과 디렉토리를 아카이브하고 압축하는 데 사용됩니다. 주로 백업이나 배포를 위해 여러 파일을 하나의 파일로 묶는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tar [options] [arguments]
```

## Common Options
- `-c`: 새로운 아카이브를 생성합니다.
- `-x`: 아카이브에서 파일을 추출합니다.
- `-f`: 아카이브 파일의 이름을 지정합니다.
- `-v`: 진행 상황을 자세히 보여줍니다 (verbose).
- `-z`: gzip으로 압축하거나 해제합니다.
- `-j`: bzip2로 압축하거나 해제합니다.

## Common Examples
- **아카이브 생성**: `myfiles` 디렉토리를 `archive.tar`라는 이름으로 아카이브합니다.
  ```bash
  tar -cvf archive.tar myfiles
  ```

- **gzip으로 압축된 아카이브 생성**: `myfiles` 디렉토리를 `archive.tar.gz`로 압축합니다.
  ```bash
  tar -czvf archive.tar.gz myfiles
  ```

- **아카이브에서 파일 추출**: `archive.tar`에서 모든 파일을 추출합니다.
  ```bash
  tar -xvf archive.tar
  ```

- **gzip으로 압축된 아카이브에서 파일 추출**: `archive.tar.gz`에서 파일을 추출합니다.
  ```bash
  tar -xzvf archive.tar.gz
  ```

- **특정 파일 추출**: `archive.tar`에서 `file1.txt`만 추출합니다.
  ```bash
  tar -xvf archive.tar file1.txt
  ```

## Tips
- 아카이브를 생성할 때 `-v` 옵션을 사용하면 어떤 파일이 추가되고 있는지 확인할 수 있어 유용합니다.
- 압축된 아카이브를 사용할 때는 `-z` 또는 `-j` 옵션을 잊지 마세요.
- 아카이브 파일을 관리하기 위해 파일 이름에 날짜를 포함시키면 좋습니다. 예: `backup_2023-10-01.tar.gz`.