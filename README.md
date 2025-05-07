# Docker Post

게시판 웹 애플리케이션의 Docker 기반 배포 프로젝트입니다. Spring Boot 백엔드와 Svelte 프론트엔드로 구성된 현대적인 웹 애플리케이션을 쉽게 배포할 수 있습니다.

## 🚀 기술 스택

### 백엔드
- **Java 21**
- **Spring Boot 3.3.5**
- **Spring Data JPA**
- **Spring Security**
- **JWT 인증**
- **MySQL 8**
- **Swagger/OpenAPI** (API 문서화)

### 프론트엔드
- **Svelte 5**
- **TypeScript**
- **Vite**
- **Tailwind CSS**
- **DayJS**

### 인프라
- **Docker**
- **Docker Compose**

## 📋 프로젝트 구조

```
docker-post/
├── backend/               # Spring Boot 백엔드
│   ├── src/               # 소스 코드
│   ├── dockerfile         # 백엔드 도커 이미지 빌드 설정
│   └── build.gradle       # Gradle 빌드 설정
├── frontend/              # Svelte 프론트엔드
│   ├── src/               # 소스 코드
│   ├── static/            # 정적 파일
│   ├── dockerfile         # 프론트엔드 도커 이미지 빌드 설정
│   └── package.json       # NPM 패키지 설정
└── docker-compose.yml     # 멀티 컨테이너 애플리케이션 설정
```

## 🔧 설치 및 실행 방법

### 요구사항
- Docker 및 Docker Compose가 설치되어 있어야 합니다.

### 실행 방법

1. 저장소 클론
   ```bash
   git clone https://github.com/yu-teacher/docker-post.git
   cd docker-post
   ```

2. Docker Compose로 애플리케이션 실행
   ```bash
   docker-compose up -d
   ```

3. 애플리케이션 접속
   - 프론트엔드: http://localhost
   - 백엔드 API: http://localhost:8080
   - Swagger UI (API 문서): http://localhost:8080/swagger-ui.html

## 🌐 주요 기능

- **게시글 관리**: 게시글 생성, 조회, 수정, 삭제
- **사용자 인증**: JWT 기반 사용자 인증 시스템
- **API 문서화**: Swagger를 통한 RESTful API 문서화

## 🛠️ 개발 환경 설정

### 백엔드 개발

```bash
cd backend
./gradlew bootRun
```

### 프론트엔드 개발

```bash
cd frontend
npm install
npm run dev
```

## 📦 배포

Docker Compose를 사용하여 모든 서비스를 함께 배포할 수 있습니다:

```bash
docker-compose up -d --build
```

## 🔒 환경 변수

### 백엔드
- `SPRING_DATASOURCE_URL`: MySQL 데이터베이스 URL
- `SPRING_DATASOURCE_USERNAME`: 데이터베이스 사용자 이름
- `SPRING_DATASOURCE_PASSWORD`: 데이터베이스 비밀번호

### 프론트엔드
- `NODE_ENV`: 노드 환경 (개발/프로덕션)
- `PORT`: 애플리케이션 포트
- `HOST`: 호스트 주소

## 📝 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.
