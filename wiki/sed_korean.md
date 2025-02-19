# [리눅스] C Shell (csh) sed 사용법: 텍스트 스트림 편집

## Overview
`sed`는 스트림 편집기(Stream Editor)로, 텍스트 데이터를 처리하고 변환하는 데 사용됩니다. 주로 파일의 내용을 수정하거나 특정 패턴을 찾아 대체하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
sed [options] [arguments]
```

## Common Options
- `-e`: 여러 개의 편집 명령을 사용할 때 사용합니다.
- `-i`: 파일을 직접 수정합니다.
- `-n`: 기본 출력 생략, 명시적으로 출력할 때만 사용합니다.
- `s/pattern/replacement/`: 패턴을 찾아 대체합니다.

## Common Examples
1. 파일에서 특정 단어를 다른 단어로 대체하기:
   ```bash
   sed 's/oldword/newword/g' filename.txt
   ```

2. 파일을 직접 수정하여 특정 단어를 대체하기:
   ```bash
   sed -i 's/oldword/newword/g' filename.txt
   ```

3. 특정 패턴이 포함된 줄만 출력하기:
   ```bash
   sed -n '/pattern/p' filename.txt
   ```

4. 여러 개의 편집 명령을 사용하기:
   ```bash
   sed -e 's/first/second/g' -e 's/third/fourth/g' filename.txt
   ```

## Tips
- `-i` 옵션을 사용할 때는 원본 파일을 백업하는 것이 좋습니다. 예를 들어, `-i.bak`를 사용하면 `.bak` 확장자를 가진 백업 파일이 생성됩니다.
- 복잡한 패턴을 사용할 때는 정규 표현식을 활용하여 더 정교한 검색 및 대체가 가능합니다.
- `sed`의 결과를 다른 명령과 파이프하여 더 복잡한 데이터 처리를 할 수 있습니다.