# :credit_card: 선결제 관리 어플

2025.01.06 ~ 2025.02.21 / 6명

메인사진 넣어야 하는데 피피티가 없어요ㅠ

## 프로젝트 소개

- PrePay는 여러 사람이 함께 사용하는 가게에 금액을 **미리 선결제하고**, QR 코드를 통해 간편하게 결제할 수 있도록 돕는 어플리케이션입니다.

- 사용자들은 그룹을 **생성하고 참여**할 수 있으며 그룹에 등록된 가게에서 **선결제된 금액을 사용하여 결제**할 수 있습니다.

- 그룹은 공개 그룹과 비공개 그룹으로 나누어져 있습니다.
  
   **공개 그룹** : 특정 사용자가 기부형식으로 가게에 금액을 선결제 하며 누구나 금액을 사용가능
  
   **비공개 그룹** : 회사나, 동아리 등 특정 사용자들만 사용 가능한 그룹으로 비밀번호를 통해 입장 가능  

## 팀원 구성

| ![Image](https://github.com/user-attachments/assets/73daf29c-815f-4935-ac6c-acbe89fcb72d) | ![Image](https://github.com/user-attachments/assets/f9cdc7f1-1ba5-40df-960a-ff344da2fddb) | ![Image](https://github.com/user-attachments/assets/d6f6a979-7125-4b29-8ba1-06c7ec13c7a4) | ![Image](https://github.com/user-attachments/assets/73daf29c-815f-4935-ac6c-acbe89fcb72d) | ![Image](https://github.com/user-attachments/assets/3a316fff-b912-461a-b8a6-dea2d16044f4) | ![Image](https://github.com/user-attachments/assets/d6f6a979-7125-4b29-8ba1-06c7ec13c7a4) |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 김기훈([@kimgihun1234](https://github.com/kimgihun1234))                                     | 차현우([@sangmin0806](https://github.com/sangmin0806))                                       | 조성윤([@SeongyunGit](https://github.com/SeongyunGit))                                       | 서현석([@minseonkkim](https://github.com/minseonkkim))                                       | 김성수([@Dufrane-S](https://github.com/Dufrane-S))                                           | 경이현([@KyungYiHyun](https://github.com/KyungYiHyun))                                       |
| 팀장 / Back End                                                                             | Front End                                                                                 | Front End                                                                                 | Front End                                                                                 | Back End                                                                                  | Front End                                                                                 |

## 1. 개발환경

- Front End : Kotlin, Android Studio

- Back End : Java17, Spring boot, Spring Data JPA, Spring Security

- Infra : Amazon EC2, Docker, Jenkins, Nginx

- DB : Mysql

- Tools : Git, Jira, Notion

## 2. 프로젝트 구조

```
C:.
├─.gradle
│  ├─8.11.1
│  │  ├─checksums
│  │  ├─executionHistory
│  │  ├─expanded
│  │  ├─fileChanges
│  │  ├─fileHashes
│  │  └─vcsMetadata
│  ├─buildOutputCleanup
│  └─vcs-1
├─.idea
│  ├─dataSources
│  │  └─4063f9e9-6a34-4c40-b20e-12ee78d77031
│  │      └─storage_v2
│  │          └─_src_
│  │              └─schema
│  └─modules
├─build
│  ├─classes
│  │  └─java
│  │      ├─main
│  │      │  └─com
│  │      │      └─d111
│  │      │          └─PrePay
│  │      │              ├─aop
│  │      │              ├─bootpay
│  │      │              │  ├─request
│  │      │              │  ├─response
│  │      │              │  └─util
│  │      │              ├─config
│  │      │              ├─controller
│  │      │              ├─dto
│  │      │              │  ├─request
│  │      │              │  └─respond
│  │      │              ├─exception
│  │      │              ├─global
│  │      │              ├─model
│  │      │              ├─repository
│  │      │              ├─schedule
│  │      │              ├─security
│  │      │              │  ├─config
│  │      │              │  ├─controller
│  │      │              │  ├─dto
│  │      │              │  ├─entity
│  │      │              │  ├─jwt
│  │      │              │  ├─oauth2
│  │      │              │  ├─repository
│  │      │              │  └─service
│  │      │              ├─service
│  │      │              └─value
│  │      └─test
│  │          └─com
│  │              └─d111
│  │                  └─PrePay
│  ├─generated
│  │  ├─querydsl
│  │  │  └─com
│  │  │      └─d111
│  │  │          └─PrePay
│  │  │              ├─model
│  │  │              └─security
│  │  │                  └─entity
│  │  └─sources
│  │      └─headers
│  │          └─java
│  │              ├─main
│  │              └─test
│  ├─libs
│  ├─reports
│  │  ├─problems
│  │  └─tests
│  │      └─test
│  │          ├─classes
│  │          ├─css
│  │          ├─js
│  │          └─packages
│  ├─resources
│  │  └─main
│  ├─test-results
│  │  └─test
│  │      └─binary
│  └─tmp
│      ├─bootJar
│      ├─compileJava
│      │  └─compileTransaction
│      │      ├─backup-dir
│      │      └─stash-dir
│      ├─compileTestJava
│      │  └─compileTransaction
│      │      ├─backup-dir
│      │      └─stash-dir
│      ├─jar
│      └─test
├─gradle
│  └─wrapper
└─src
    ├─main
    │  ├─java
    │  │  └─com
    │  │      └─d111
    │  │          └─PrePay
    │  │              ├─aop
    │  │              ├─bootpay
    │  │              │  ├─request
    │  │              │  ├─response
    │  │              │  └─util
    │  │              ├─config
    │  │              ├─controller
    │  │              ├─dto
    │  │              │  ├─request
    │  │              │  └─respond
    │  │              ├─exception
    │  │              ├─global
    │  │              ├─model
    │  │              ├─repository
    │  │              ├─schedule
    │  │              ├─security
    │  │              │  ├─config
    │  │              │  ├─controller
    │  │              │  ├─dto
    │  │              │  ├─entity
    │  │              │  ├─jwt
    │  │              │  ├─oauth2
    │  │              │  ├─repository
    │  │              │  └─service
    │  │              ├─service
    │  │              └─value
    │  └─resources
    └─test
        └─java
            └─com
                └─d111
                    └─PrePay
```

## 3. 역할 분담

역할 분담 사진 피피티가 없어요ㅠ

## 4. 핵심 기능 소개

#### [메인페이지]

![Image](https://github.com/user-attachments/assets/74314c36-bac3-44cf-b6b8-9529c05cee61)

#### [그룹 생성]

![Image](https://github.com/user-attachments/assets/c376c359-81b2-4786-a6af-a725605ea5c9)

#### [공개 그룹 조회]

![Image](https://github.com/user-attachments/assets/e4e12709-5185-40f9-9a40-1bb25b113abb)

#### [QR 결제]

![Image](https://github.com/user-attachments/assets/2aefd194-b5ac-44b3-84ba-5aa566f277ad)

#### [결제 내역 조회]

![Image](https://github.com/user-attachments/assets/2dc4a7c2-3b24-48d4-9f38-9c56b286cfe9)

## 5. 시스템 아키텍쳐

![Image](https://github.com/user-attachments/assets/23ae6ef7-89a1-44f2-8abe-28af51c9fe89)

## 6. 프로젝트 후기
