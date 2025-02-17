# [리눅스] Bash sqlite3 사용법: SQLite 데이터베이스 관리

## Overview
sqlite3 명령어는 SQLite 데이터베이스를 생성하고 관리하는 데 사용됩니다. 이 명령어를 통해 데이터베이스에 쿼리를 실행하고, 테이블을 생성하거나 수정하며, 데이터를 삽입하고 조회할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: 사용 가능한 모든 옵션과 명령어를 표시합니다.
- `-version`: 현재 설치된 SQLite의 버전을 표시합니다.
- `-init <file>`: 지정된 파일을 실행하여 데이터베이스를 초기화합니다.
- `-batch`: 대화형 모드를 비활성화하고, 스크립트 모드로 실행합니다.

## Common Examples
- 데이터베이스 파일 생성 및 접속:
```bash
sqlite3 mydatabase.db
```

- 테이블 생성:
```bash
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
```

- 데이터 삽입:
```bash
sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
```

- 데이터 조회:
```bash
sqlite3 mydatabase.db "SELECT * FROM users;"
```

- 데이터베이스 백업:
```bash
sqlite3 mydatabase.db ".backup mydatabase_backup.db"
```

## Tips
- 데이터베이스를 작업하기 전에 항상 백업을 해두는 것이 좋습니다.
- SQL 쿼리를 작성할 때는 세미콜론(;)을 잊지 말고 추가하세요.
- `.exit` 명령어를 사용하여 sqlite3 세션을 종료할 수 있습니다.