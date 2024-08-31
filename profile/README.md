<p align="center"><img src="https://capsule-render.vercel.app/api?type=Waving&color=0099f9&fontColor=ffffff&height=150&section=footer&text=SolSolHigh&fontSize=70"></p>

# FE

### 팀원 역할

---

| 이름   | 역할                                         |
| ------ | -------------------------------------------- |
| 조성우 | Mocking, API 설계 및 관리, 요구사항 구현     |
| 양규현 | 프로젝트 관리, Storybook 관리, 요구사항 구현 |
| 최요하 | 인프라, 깃허브 관리, 요구사항 구현           |

<br>

### 개발 환경

---

| 항목               | 버전    |
| :----------------- | :------ |
| Node               | 20.16.0 |
| Npm                | 10.8.1  |
| React              | 18      |
| TypeScript         | 5.5.4   |
| Visual Studio Code | 1.92    |

<br>

### 개발 도구

---

| 항목             | 도구               |
| :--------------- | :----------------- |
| 형상 관리        | GitHub             |
| 협업 & 문서 관리 | Notion             |
| 디자인           | Figma              |
| IDE              | Visual Studio Code |

<br>

### Tech Stack

---

**Develop** <br><br>
<img src="./docs/react.svg" alt="react" width="60" height="60" />&emsp;
<img src="./docs/typescript.svg" alt="typescript" width="60" height="60" />&emsp;
<img src="./docs/storybook.svg" alt="storybook" width="60" height="60" />&emsp;
<img src="./docs/tailwindcss.svg" alt="tailwindcss" width="60" height="60" />&emsp;
<img src="./docs/tanstackquery.png" alt="tanstack-query" width="60" height="60" />&emsp;
<img src="./docs/recoil.svg" alt="recoil" width="60" height="60" />&emsp;
<br>
<br>
**CI/CD**<br><br>
<img src="./docs/githubactions.svg" alt="githubactions" width="60" height="60" />&emsp;
<img src="./docs/docker.svg" alt="docker" width="60" height="60" />&emsp;
<img src="./docs/nginx.svg" alt="nginx" width="60" height="60" />&emsp;
<img src="./docs/ec2.svg" alt="ec2" width="60" height="60" />

<br>

### Wiki

---

[Project Convention](https://github.com/SolSolHigh/SolSolHigh-FE/wiki/SolSolHigh%E2%80%90FE-Project-Convention)<br>
[GitHub Convention](https://github.com/SolSolHigh/SolSolHigh-FE/wiki/SolSolHigh%E2%80%90FE-GitHub-Repository-Convention)


<br>
<br>

### 빌드 및 실행 방법

---

```jsx
#!/bin/bash
cd ~/solsol-high/static
git fetch origin
git checkout $1
git pull origin $1
cd ~/solsol-high/static/ssh-web
npm install
npm run build
```

- 위의 스크립트를 실행시키는 쉘 스크립트 파일을 웹 프로젝트를 배포하고자 하는 서버에 심어놓는다.

```jsx

name: SolSolHigh-FE Deploy

on:
  push:
    branches: develop

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      # stage : ssh
      - name: SSH
        uses: appleboy/ssh-action@v1.0.3
        with:
          host: ${{ secrets.SSH_KRO_HOST }}
          username: ${{ secrets.SSH_KRO_USERNAME }}
          password: ${{ secrets.SSH_PASSWORD }}
          script: |
            cd ~/solsol-high
            ./static.sh develop
```

- develop 브랜치에 push 이벤트가 발생하면 서버로 통합 후 배포
- 웹 프로젝트를 배포하고자 하는 서버에 SSH 로 접속한다.
- 위에서 작성한 쉘 스크립트를 실행시킨다.

<br>
<br>
<br>
<br>

# BE

### 팀원 역할

---

| 이유승                                                                           | 김현진                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <img src="https://avatars.githubusercontent.com/u/105223190?v=4" width="220"> | <img src="https://avatars.githubusercontent.com/u/68643347?v=4" width="220"> |
| 인프라, 요구사항 구현, 테스팅                                                             | AI, API 문서 관리, 요구사항 구현, 테스팅                                                  |

<br>

### 개발 환경

---

| 항목                       | 버전       |
|:-------------------------|:---------|
| Java corretto            | 17.0.4.1 |
| Spring Boot              | 3.3.2    |
| Intellij Ultimate        | 2024.2   |
| MySQL                    | 8.3.0    |
| Docker                   | 24.0.2   |
| nginx                    | 1.26     |
| redis                    | 5.0.7    |
| firebase cloud messaging | 9.3.0    |

<br>

### 개발 도구

---

| 항목         | 도구       |
|:-----------|:---------|
| 형상 관리      | GitHub   |
| 협업 & 문서 관리 | Notion   |
| IDE        | Intellij |

<br>

### Tech Stack

---

**Develop** <br><br>
<img src="https://img.shields.io/badge/Java-333333?style=for-the-badge&logo=openjdk&logoColor=orange">&emsp;
<img src="https://img.shields.io/badge/Spring boot-333333?style=for-the-badge&logo=springboot&logoColor=green">&emsp;
<img src="https://img.shields.io/badge/Spring Security-333333?style=for-the-badge&logo=springsecurity&logoColor=green">
&emsp;
<img src="https://img.shields.io/badge/Spring Data JPA-333333?style=for-the-badge&logo=hibernate&logoColor=green">&emsp;
<img src="https://img.shields.io/badge/OpenAI-333333?style=for-the-badge&logo=openai&logoColor=gray">&emsp;
<img src="https://img.shields.io/badge/MySQL-333333?style=for-the-badge&logo=mysql&logoColor=blue">&emsp;
<img src="https://img.shields.io/badge/Redis-333333?style=for-the-badge&logo=redis&logoColor=red">&emsp;
<img src="https://img.shields.io/badge/gradle-333333?style=for-the-badge&logo=gradle&logoColor=darkgreen">&emsp;
<img src="https://img.shields.io/badge/FCM-333333?style=for-the-badge&logo=firebase&logoColor=orange">&emsp;

<br>
<br>

**Infra**<br><br>
<img src="https://img.shields.io/badge/docker-333333?style=for-the-badge&logo=docker&logoColor=blue">&emsp;
<img src="https://img.shields.io/badge/ubuntu-333333?style=for-the-badge&logo=ubuntu&logoColor=orage">&emsp;
<img src="https://img.shields.io/badge/nginx-333333?style=for-the-badge&logo=nginx&logoColor=green">&emsp;
<img src="https://img.shields.io/badge/jenkins-333333?style=for-the-badge&logo=jenkins&logoColor=orange">&emsp;
<img src="https://img.shields.io/badge/s3-333333?style=for-the-badge&logo=amazon&logoColor=orange">&emsp;

### 환경 변수

---

**./docker-compose.yml**
```yml

services:
  solsol-app:
    container_name: solsol-app
    build: .
    ports:
      - "8080:8080"
    depends_on:
      - solsol-mysql
      - solsol-redis
    environment:
      SPRING_DATASOURCE_URL: jdbc:mysql://solsol-mysql:3306/solsolhigh
      SPRING_DATASOURCE_USERNAME: "root"
      SPRING_DATASOURCE_PASSWORD: # DB 비밀번호 작성
      TZ: "Asia/Seoul"
    restart: always
    networks:
      - internal_network

  solsol-mysql:
    container_name: solsol-mysql
    image: mysql
    ports:
      - "3307:3306"
    environment:
      MYSQL_DATABASE: solsolhigh
      MYSQL_ROOT_HOST: '%'
      MYSQL_ROOT_PASSWORD: # DB 비밀번호 작성
      TZ: "Asia/Seoul"
    healthcheck:
      test: [ 'CMD-SHELL', 'mysqladmin ping -h 127.0.0.1 -u root --password=$MYSQL_ROOT_PASSWORD' ]
      interval: 10s
      timeout: 2s
      retries: 100
    volumes:
      - ~/solsol-high/database/mysql:/var/lib/mysql
    networks:
      - internal_network

  solsol-redis:
    image: redis
    container_name: solsol-redis
    ports:
      - "6380:6379"
    networks:
      - internal_network

networks:
  internal_network:
```



**src/main/resources/application.yml**

```yml
server:
  servlet:
    encoding:
      charset: UTF-8

spring:
  profiles:
    include: dev, oauth, secret
  jpa:
    show-sql: true
    open-in-view: false 
    hibernate:
      ddl-auto: none
    properties:
      hibernate:
        highlight_sql: true
        format_sql: true
        default_batch_fetch_size: 100
  sql:
    init:
      mode: always
  servlet:
    multipart:
      max-file-size: 50MB
      max-request-size: 50MB
```

<br>

**src/main/resources/application-dev.yml**

```yml

solsol:
  front:
    base: # 프론트 서버 주소

masterbank:
  api-key: # 싸피 금융망 api key
  base: # 싸피 금융망 api url
  institution-code: #기관 코드
  fintech-app-no: # 핀테크 앱 일렬번호

```

<br>

**src/main/resources/application-oauth.yml**

```yml

spring:
  security:
    oauth2:
      client:
        registration:
          naver:
            client-name: naver
            client-id: 
            client-secret: 
            redirect-uri: http://localhost:8080/login/oauth2/code/naver
            authorization-grant-type: authorization_code
            scope: name, email
          kakao:
            client-name: kakao
            client-id: 
            client-secret: 
            redirect-uri: http://localhost:8080/login/oauth2/code/kakao
            authorization-grant-type: authorization_code
            client-authentication-method: client_secret_post
            scope: account_email, name
        provider:
          naver:
            authorization-uri: https://nid.naver.com/oauth2.0/authorize
            token-uri: https://nid.naver.com/oauth2.0/token
            user-info-uri: https://openapi.naver.com/v1/nid/me
            user-name-attribute: response
          kakao:
            authorization-uri: https://kauth.kakao.com/oauth/authorize
            token-uri: https://kauth.kakao.com/oauth/token
            user-info-uri: https://kapi.kakao.com/v2/user/me
            user-name-attribute: id

```

<br>

**application-secret.yml**
```yml

spring:
  ai:
    openai:
      api-key: # openai 에서 발급받은 키

cloud:
  aws:
    credentials:
      access-key: # IAM 발급받은 엑세스 키
      secret-key: # IAM 발급받은 비밀 키
    s3:
      bucket: # s3 버킷이름
    region:
      static: # s3 지역
    stack:
      auto: false

```

<br>
<br>

### 빌드 및 실행방법
---
    yaml 파일 모두 필요한 값들 채운 후 필요한 위치로 전송.
    docker 설치 후 docker-compose.yml가 존재하는 경로로 이동.
    docker-compose up -d 실행.
---


### ERD
<img width="1280" alt="스크린샷 2024-08-31 오후 4 21 19" src="https://github.com/user-attachments/assets/da6abbb0-4ff5-40ec-8c69-948cba852f87">
