# [리눅스] Bash psql 사용법: PostgreSQL 데이터베이스에 접근하기

## Overview
`psql` 명령은 PostgreSQL 데이터베이스에 접근하고 쿼리를 실행할 수 있는 명령줄 인터페이스입니다. 이 도구를 사용하면 데이터베이스를 관리하고, 데이터를 조회하며, SQL 명령을 실행할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
psql [options] [arguments]
```

## Common Options
- `-h`: 데이터베이스 서버의 호스트 이름을 지정합니다.
- `-p`: 데이터베이스 서버의 포트 번호를 지정합니다.
- `-U`: 데이터베이스 사용자 이름을 지정합니다.
- `-d`: 연결할 데이터베이스의 이름을 지정합니다.
- `-f`: SQL 파일을 실행합니다.

## Common Examples
1. PostgreSQL 데이터베이스에 연결하기:
   ```bash
   psql -h localhost -U username -d database_name
   ```

2. SQL 파일 실행하기:
   ```bash
   psql -U username -d database_name -f script.sql
   ```

3. 데이터베이스 목록 보기:
   ```bash
   psql -U username -d database_name -c "\l"
   ```

4. 테이블의 데이터 조회하기:
   ```bash
   psql -U username -d database_name -c "SELECT * FROM table_name;"
   ```

## Tips
- `\?` 명령어를 입력하면 psql에서 사용할 수 있는 모든 명령어 목록을 확인할 수 있습니다.
- `\q`를 입력하면 psql 세션을 종료할 수 있습니다.
- 쿼리를 작성할 때 세미콜론(`;`)을 잊지 마세요. 쿼리의 끝을 나타내는 중요한 요소입니다.