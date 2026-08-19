# sandbox

게시판(board)을 소재로 다양한 기술을 실험하고 학습하는 프로젝트입니다. 각 실험은 GitHub 이슈로 시작해 PR로 정리하며, 블로그처럼 기록을 남깁니다.

## 스택

- 백엔드: Java 21, Spring Boot, Gradle(Kotlin DSL), Spring Data JPA + Hibernate
- 프론트엔드: Next.js, TypeScript
- DB: MySQL (로컬은 Docker Compose)

## 구조

```
backend/    Spring Boot 프로젝트
frontend/   Next.js 프로젝트
docker-compose.yml   로컬 MySQL
```

## 로컬 실행

### DB

로컬에 이미 3306(mysqld), 33060(mysqld X Protocol), 3307(다른 프로젝트 컨테이너) 포트가 사용 중일 수 있어, 호스트 포트는 3308로 매핑되어 있습니다.

```bash
docker compose up -d
```

### 백엔드

```bash
cd backend
./gradlew bootRun
```

### 프론트엔드

```bash
cd frontend
npm install
npm run dev
```

## 워크플로우

- 새 실험/기능은 이슈를 먼저 만들고 `feature/#<이슈번호>-<설명>` 브랜치에서 작업합니다.
- 작업 완료 후 PR로 정리하며, 무엇을 왜 시도했는지와 배운 점을 PR 본문에 남깁니다.
