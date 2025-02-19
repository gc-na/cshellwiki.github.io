# [리눅스] C Shell (csh) modprobe 사용법: 모듈을 로드하거나 언로드하는 명령

## Overview
`modprobe` 명령은 리눅스 커널 모듈을 로드하거나 언로드하는 데 사용됩니다. 이 명령은 의존성을 자동으로 처리하여 필요한 모듈을 함께 로드할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
modprobe [options] [arguments]
```

## Common Options
- `-r`, `--remove`: 지정한 모듈을 언로드합니다.
- `-n`, `--dry-run`: 실제로 모듈을 로드하거나 언로드하지 않고 어떤 일이 일어날지를 보여줍니다.
- `-v`, `--verbose`: 자세한 출력을 제공합니다.
- `--show`: 로드할 모듈의 정보를 표시합니다.

## Common Examples
다음은 `modprobe` 명령의 몇 가지 실용적인 예입니다.

1. 모듈 로드하기:
   ```bash
   modprobe <module_name>
   ```

2. 모듈 언로드하기:
   ```bash
   modprobe -r <module_name>
   ```

3. 로드할 모듈의 의존성 확인하기:
   ```bash
   modprobe --show <module_name>
   ```

4. 실제로 모듈을 로드하지 않고 어떤 일이 일어날지를 확인하기:
   ```bash
   modprobe -n <module_name>
   ```

## Tips
- 모듈을 로드하기 전에 항상 의존성을 확인하세요.
- `-v` 옵션을 사용하여 모듈 로드 과정에서 발생하는 문제를 쉽게 파악할 수 있습니다.
- 시스템 부팅 시 자동으로 로드해야 하는 모듈은 `/etc/modules` 파일에 추가하세요.