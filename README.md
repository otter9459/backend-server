# cumadi

### 마크다운을 활용해 블로그 포스트를 작성할 수 있으며, 해당 포스트를 시리즈로 묶어 판매할 수 있는 사이트입니다.

블로그 포스트 작성에 마크다운을 적용할 수 있고 이를 시리즈라는 개념으로 목록화 시킬 수 있습니다.
<br>
시리즈라는 이름으로 목록화된 포스트는 원하는 가격에 판매가 가능합니다.
<br>
이외에도 작성자의 의도에 따라 무료로 공개되어 있는 포스트도 확인 할 수 있습니다.

이러한 기능들을 통해 다양한 지식의 공유를 활성화 시키는 것이 주 목적인 서비스입니다.

<br>

# Issue & Pull-request

https://github.com/mcb-backend/backend-server

<br>

# 기술 스택

![](https://img.shields.io/badge/Back-Typescript-3178C6?style=for-the-badge&logo=Typescript)

![](https://img.shields.io/badge/Back-Node.Js-339933?style=for-the-badge&logo=Node.js)

![](https://img.shields.io/badge/Back-nestjs-DD0031?style=for-the-badge&logo=Nestjs&logoColor=DD0031)

![](https://img.shields.io/badge/Back-graphql-E10098?style=for-the-badge&logo=graphql&logoColor=E10098)

![](https://img.shields.io/badge/Back-TypeORM-E34F26?style=for-the-badge)

![](https://img.shields.io/badge/db-redis-CC342D?style=for-the-badge&logo=redis)

![](https://img.shields.io/badge/db-mysql-4479A1?style=for-the-badge&logo=mysql)

![](https://img.shields.io/badge/dev-aws-E95420?style=for-the-badge&logo=amazonaws&logoColor=E95420)

![](https://img.shields.io/badge/dev-GCP-4285F4?style=for-the-badge&logo=googlecloud)

![](https://img.shields.io/badge/dev-docker_compose-2496ED?style=for-the-badge&logo=docker)

<br>

# 담당 파트

### 공동 구현<br>

- Database ERD 작성<br>
- GCP VM instance 배포<br>
  - Docker-compose 활용<br>

<br>

### Backend<br>

- ### 유저 API

  - User CRUD API<br>
    - JWT Token 활용 보안 강화 (Access, Refresh)<br>
    - Redis 활용 블랙리스트 로그아웃 기능 구현<br>
  - Auth 관련 API
    - gql-guard 활용, 로그인 여부 등 검증
  - 소셜 로그인 API
    - OAuth 라이브러리 활용, 각 provider를 구분할 수 있도록 guard 모듈화

- ### 게시글, 댓글, 메모 등 관련 API

  - Memo CRUD API<br>
  - Post CRUD API<br>
  - Tags CRUD API<br>
  - Statistics CRUD API<br>
    - 한국 서버의 시간(00:00), 날짜를 기준으로 조회수 기록
  - Comment CRUD API<br>
  - Answer CRUD API

- ### 이미지 업로드 API
  - Image Upload용 API<br>
    - graphql-upload 라이브러리 활용, AWS-S3 storage로 이미지를 업로드하기 위한 API 구현

<br>

### devops<br>

- AWS S3 Image bucket 생성<br>
- GCP SQL 기반 MySQL DB 생성 및 배포

<br><br>

# Database ERD

![cumadi_ERD](https://github.com/otter9459/backend-server/blob/main/public/cumadi_ERD.png?raw=true)

<br><br>

# Backend System-Architecture

![cumadi_system_arcitecture](https://github.com/otter9459/backend-server/blob/main/public/%E2%80%8Ecumadi_system_arcitecture.png?raw=true)
