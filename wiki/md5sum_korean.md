# [리눅스] C Shell (csh) md5sum 사용법: 파일의 MD5 해시 생성

## Overview
md5sum 명령은 파일의 MD5 해시 값을 생성하는 데 사용됩니다. 이 해시는 파일의 무결성을 확인하는 데 유용하며, 파일이 변경되지 않았는지 검증하는 데 도움을 줍니다.

## Usage
기본 구문은 다음과 같습니다:
```csh
md5sum [옵션] [인수]
```

## Common Options
- `-b`: 바이너리 파일을 처리합니다.
- `-c`: 체크섬 파일을 사용하여 파일의 무결성을 검사합니다.
- `-t`: 텍스트 파일을 처리합니다.

## Common Examples
- 파일의 MD5 해시 생성:
```csh
md5sum myfile.txt
```

- 여러 파일의 MD5 해시 생성:
```csh
md5sum file1.txt file2.txt file3.txt
```

- 체크섬 파일을 사용하여 파일 무결성 검사:
```csh
md5sum -c checksum.md5
```

- 바이너리 파일의 MD5 해시 생성:
```csh
md5sum -b binaryfile.bin
```

## Tips
- 해시 값을 저장할 때는 출력 결과를 파일로 리디렉션하여 나중에 사용할 수 있습니다.
- 파일의 변경 여부를 확인할 때는 항상 원본 해시와 비교하는 것이 좋습니다.
- md5sum은 대용량 파일에 대해서도 빠르게 해시를 생성할 수 있으므로, 대량의 파일 검증에 유용합니다.