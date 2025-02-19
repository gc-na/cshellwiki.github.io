# [리눅스] C Shell (csh) case 사용법: 조건에 따라 명령 실행

## Overview
`case` 명령은 주어진 패턴에 따라 명령을 실행하는 데 사용됩니다. 이는 특정 문자열이나 변수의 값을 기반으로 여러 조건을 처리할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:
```
case [변수] in
    [패턴1])
        [명령1]
        ;;
    [패턴2])
        [명령2]
        ;;
    ...
esac
```

## Common Options
- `*`: 모든 문자열과 일치하는 패턴.
- `?`: 단일 문자와 일치하는 패턴.
- `[...]`: 대괄호 안의 문자 중 하나와 일치하는 패턴.

## Common Examples
1. **문자열에 따라 다른 메시지 출력하기**
   ```csh
   set fruit = "apple"
   switch ($fruit) 
   case "apple":
       echo "사과입니다."
       breaksw
   case "banana":
       echo "바나나입니다."
       breaksw
   default:
       echo "알 수 없는 과일입니다."
   endsw
   ```

2. **파일 확장자에 따라 다른 명령 실행하기**
   ```csh
   set file = "document.txt"
   case ($file) in
       *.txt)
           echo "텍스트 파일입니다."
           ;;
       *.jpg)
           echo "이미지 파일입니다."
           ;;
       *)
           echo "알 수 없는 파일 형식입니다."
           ;;
   esac
   ```

3. **사용자 입력에 따라 다른 작업 수행하기**
   ```csh
   set response = $1
   case ($response) in
       "y" | "Y")
           echo "계속 진행합니다."
           ;;
       "n" | "N")
           echo "작업을 중단합니다."
           ;;
       *)
           echo "잘못된 입력입니다."
           ;;
   esac
   ```

## Tips
- `case` 명령은 여러 조건을 간단하게 처리할 수 있어 코드의 가독성을 높입니다.
- 패턴을 명확하게 정의하여 예기치 않은 입력을 방지하세요.
- `*`와 `?`를 적절히 사용하여 유연한 조건을 설정할 수 있습니다.