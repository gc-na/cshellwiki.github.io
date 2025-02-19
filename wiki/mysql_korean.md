# [리눅스] C Shell (csh) mysql 사용법: 데이터베이스 관리 및 쿼리 실행

## Overview
mysql 명령어는 MySQL 데이터베이스 관리 시스템에 접속하여 데이터베이스를 관리하고 쿼리를 실행하는 데 사용됩니다. 이 명령어를 통해 사용자는 데이터베이스에 연결하고, SQL 쿼리를 실행하며, 데이터베이스 구조를 수정할 수 있습니다.

## Usage
mysql 명령어의 기본 구문은 다음과 같습니다:

```bash
mysql [options] [arguments]
```

## Common Options
- `-u [username]`: MySQL 사용자 이름을 지정합니다.
- `-p`: 비밀번호 입력을 요청합니다.
- `-h [hostname]`: MySQL 서버의 호스트 이름을 지정합니다.
- `-D [database]`: 연결할 데이터베이스를 지정합니다.
- `-e "[query]"`: SQL 쿼리를 직접 실행합니다.

## Common Examples
다음은 mysql 명령어의 몇 가지 일반적인 사용 예입니다.

1. MySQL 서버에 접속하기:
   ```bash
   mysql -u root -p
   ```

2. 특정 데이터베이스에 접속하기:
   ```bash
   mysql -u user -p -D mydatabase
   ```

3. SQL 쿼리 실행하기:
   ```bash
   mysql -u user -p -e "SELECT * FROM mytable;"
   ```

4. 데이터베이스 목록 보기:
   ```bash
   mysql -u user -p -e "SHOW DATABASES;"
   ```

## Tips
- 비밀번호를 명령어에 직접 입력하는 것은 보안상 위험하므로 `-p` 옵션만 사용하고 비밀번호 입력을 요청받는 것이 좋습니다.
- 쿼리를 실행할 때는 세미콜론(;)으로 쿼리의 끝을 명시해야 합니다.
- 데이터베이스 작업을 수행하기 전에 항상 데이터의 백업을 유지하는 것이 좋습니다.