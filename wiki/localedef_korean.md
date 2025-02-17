# [리눅스] Bash localedef 사용법: 로케일 정의 생성

## Overview
`localedef` 명령어는 시스템에서 사용할 로케일을 정의하고 생성하는 데 사용됩니다. 로케일은 언어, 지역 및 문자 집합에 대한 정보를 포함하여 프로그램이 데이터를 어떻게 표시하고 처리할지를 결정합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
localedef [options] [arguments]
```

## Common Options
- `-i, --inputfile`: 입력 파일을 지정합니다.
- `-c, --charset`: 문자 집합을 지정합니다.
- `-v, --verbose`: 자세한 출력을 표시합니다.
- `-f, --file`: 로케일 정의 파일을 지정합니다.

## Common Examples
로케일을 생성하는 몇 가지 예시는 다음과 같습니다.

1. 기본 로케일 생성:
   ```bash
   localedef -i ko_KR -f UTF-8 ko_KR.UTF-8
   ```

2. 특정 문자 집합으로 로케일 생성:
   ```bash
   localedef -i en_US -f ISO-8859-1 en_US.ISO-8859-1
   ```

3. 로케일 생성 시 자세한 정보 출력:
   ```bash
   localedef -v -i fr_FR -f UTF-8 fr_FR.UTF-8
   ```

## Tips
- 로케일을 생성한 후, `locale -a` 명령어를 사용하여 생성된 로케일 목록을 확인할 수 있습니다.
- 로케일 파일은 `/usr/lib/locale/` 또는 `/usr/share/i18n/locales/` 경로에 위치합니다.
- 로케일을 변경한 후에는 시스템을 재시작하거나 세션을 새로 고쳐야 적용됩니다.