# [리눅스] C Shell (csh) psql 사용법: PostgreSQL 데이터베이스에 연결하고 쿼리 실행

## 개요
`psql`은 PostgreSQL 데이터베이스와 상호작용하기 위한 명령줄 인터페이스입니다. 이 도구를 사용하면 SQL 쿼리를 실행하고 데이터베이스를 관리할 수 있습니다.

## 사용법
기본 구문은 다음과 같습니다:
```bash
psql [options] [arguments]
```

## 일반 옵션
- `-h`: 데이터베이스 서버의 호스트 이름을 지정합니다.
- `-p`: 데이터베이스 서버의 포트를 지정합니다.
- `-U`: 데이터베이스 사용자 이름을 지정합니다.
- `-d`: 연결할 데이터베이스의 이름을 지정합니다.
- `-f`: SQL 파일을 실행합니다.

## 일반 예제
- PostgreSQL 데이터베이스에 연결하기:
```bash
psql -U username -d database_name
```

- 특정 호스트와 포트로 연결하기:
```bash
psql -h localhost -p 5432 -U username -d database_name
```

- SQL 파일 실행하기:
```bash
psql -U username -d database_name -f script.sql
```

- 데이터베이스에서 테이블 목록 보기:
```bash
psql -U username -d database_name -c "\dt"
```

## 팁
- `\q` 명령어를 사용하여 psql 세션을 종료할 수 있습니다.
- `\h`를 입력하면 SQL 명령어에 대한 도움말을 볼 수 있습니다.
- 쿼리를 실행하기 전에 항상 데이터베이스를 백업하는 것을 권장합니다.