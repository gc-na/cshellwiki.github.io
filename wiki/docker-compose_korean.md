# [리눅스] C Shell (csh) docker-compose 사용법: 도커 컨테이너 관리

## 개요
docker-compose는 여러 개의 도커 컨테이너를 정의하고 실행할 수 있게 해주는 도구입니다. YAML 파일을 사용하여 애플리케이션의 서비스, 네트워크 및 볼륨을 설정하고, 이를 통해 복잡한 애플리케이션을 쉽게 관리할 수 있습니다.

## 사용법
기본 구문은 다음과 같습니다:
```bash
docker-compose [options] [arguments]
```

## 일반 옵션
- `up`: 정의된 서비스와 컨테이너를 시작합니다.
- `down`: 실행 중인 서비스와 컨테이너를 중지하고 제거합니다.
- `build`: 서비스의 이미지를 빌드합니다.
- `logs`: 서비스의 로그를 출력합니다.
- `ps`: 현재 실행 중인 컨테이너 목록을 표시합니다.

## 일반 예제
1. **서비스 시작하기**
   ```bash
   docker-compose up
   ```

2. **서비스 중지 및 제거하기**
   ```bash
   docker-compose down
   ```

3. **이미지 빌드하기**
   ```bash
   docker-compose build
   ```

4. **로그 보기**
   ```bash
   docker-compose logs
   ```

5. **실행 중인 컨테이너 목록 확인하기**
   ```bash
   docker-compose ps
   ```

## 팁
- **YAML 파일 관리**: `docker-compose.yml` 파일을 잘 구조화하여 서비스 간의 의존성을 명확히 하세요.
- **환경 변수 사용**: `.env` 파일을 사용하여 환경 변수를 관리하면 설정을 더 유연하게 조정할 수 있습니다.
- **백그라운드 실행**: `docker-compose up -d` 명령어를 사용하면 컨테이너를 백그라운드에서 실행할 수 있습니다.