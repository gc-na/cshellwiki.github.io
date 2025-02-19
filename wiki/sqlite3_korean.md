# [운영체제] C Shell (csh) sqlite3 사용법: SQLite 데이터베이스 관리

## 개요
sqlite3 명령어는 SQLite 데이터베이스를 생성하고 관리하는 데 사용됩니다. 이 명령어를 통해 데이터베이스에 쿼리를 실행하고, 테이블을 생성하며, 데이터를 삽입하고 조회할 수 있습니다.

## 사용법
기본 구문은 다음과 같습니다:

```csh
sqlite3 [옵션] [인수]
```

## 일반적인 옵션
- `-help`: 사용 가능한 모든 옵션과 명령어를 보여줍니다.
- `-version`: SQLite의 버전을 출력합니다.
- `-init <파일>`: 지정된 SQL 파일을 실행하여 데이터베이스를 초기화합니다.
- `-batch`: 배치 모드로 실행하여 사용자 입력 없이 명령어를 처리합니다.

## 일반적인 예제
- 데이터베이스 파일 생성 및 열기:
```csh
sqlite3 mydatabase.db
```

- 테이블 생성:
```csh
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
```

- 데이터 삽입:
```csh
sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
```

- 데이터 조회:
```csh
sqlite3 mydatabase.db "SELECT * FROM users;"
```

- 데이터베이스 종료:
```csh
sqlite3 mydatabase.db ".exit"
```

## 팁
- 데이터베이스 작업을 수행하기 전에 항상 백업을 만들어 두세요.
- SQL 쿼리를 작성할 때는 세미콜론(;)으로 명령어를 끝내는 것을 잊지 마세요.
- `.help` 명령어를 사용하여 sqlite3의 다양한 명령어와 옵션을 확인할 수 있습니다.