# [리눅스] Bash mysql 사용법: MySQL 데이터베이스 관리

## Overview
`mysql` 명령어는 MySQL 데이터베이스에 접속하고 SQL 쿼리를 실행할 수 있는 클라이언트 프로그램입니다. 이 명령어를 사용하여 데이터베이스를 관리하고, 데이터를 조회하거나 수정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
mysql [options] [arguments]
```

## Common Options
- `-u, --user`: MySQL 사용자 이름을 지정합니다.
- `-p, --password`: 비밀번호를 입력합니다. 비밀번호는 명령어 입력 후 프롬프트에서 요청됩니다.
- `-h, --host`: MySQL 서버의 호스트 이름을 지정합니다.
- `-D, --database`: 접속할 데이터베이스 이름을 지정합니다.
- `-e, --execute`: 실행할 SQL 쿼리를 직접 입력합니다.

## Common Examples
1. MySQL 서버에 접속하기:
   ```bash
   mysql -u username -p
   ```

2. 특정 데이터베이스에 접속하기:
   ```bash
   mysql -u username -p -D database_name
   ```

3. SQL 쿼리 실행하기:
   ```bash
   mysql -u username -p -e "SELECT * FROM table_name;"
   ```

4. 데이터베이스 백업하기:
   ```bash
   mysqldump -u username -p database_name > backup.sql
   ```

5. 데이터베이스 복원하기:
   ```bash
   mysql -u username -p database_name < backup.sql
   ```

## Tips
- 비밀번호를 명령어에 직접 입력하는 것은 보안상 좋지 않으므로, `-p` 옵션만 사용하고 프롬프트에서 입력하는 것이 좋습니다.
- SQL 쿼리를 실행할 때는 세미콜론(;)으로 쿼리를 종료해야 합니다.
- `--execute` 옵션을 사용하면 간단한 쿼리를 한 줄로 실행할 수 있어 편리합니다.