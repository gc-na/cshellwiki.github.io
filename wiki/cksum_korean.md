# [리눅스] C Shell (csh) cksum 사용법: 파일의 체크섬 계산

## Overview
`cksum` 명령어는 파일의 체크섬과 바이트 수를 계산하여 출력하는 데 사용됩니다. 이 명령어는 파일의 무결성을 확인하거나 파일이 변경되었는지 여부를 판단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```csh
cksum [options] [arguments]
```

## Common Options
- `-a` : 체크섬 알고리즘을 지정합니다.
- `-b` : 바이트 수를 출력합니다.
- `-h` : 도움말 메시지를 출력합니다.

## Common Examples
- 파일의 체크섬 계산하기:
```csh
cksum myfile.txt
```

- 여러 파일의 체크섬 계산하기:
```csh
cksum file1.txt file2.txt file3.txt
```

- 체크섬 알고리즘 지정하기:
```csh
cksum -a md5 myfile.txt
```

## Tips
- 체크섬을 비교하여 파일의 변경 여부를 확인할 수 있습니다.
- 대량의 파일을 처리할 때는 결과를 파일로 리다이렉트하여 저장하는 것이 유용합니다.
- 체크섬 알고리즘을 변경하여 더 강력한 무결성 검사를 수행할 수 있습니다.