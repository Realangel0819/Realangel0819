# AlwaysNight | Backend Developer

꾸준히 고민하고, 직접 구현하며, 테스트를 통해 문제를 검증하는 개발자입니다.

문제를 발견하는 데서 그치지 않고 원인을 분석하고, 해결 방법을 구현한 뒤 결과를 확인하는 과정을 중요하게 생각합니다.

---

## About Me

- Backend Development — Spring Boot 기반 REST API 및 멀티모듈 서비스 설계
- Distributed Systems — gRPC, Kafka, Redis를 활용한 서비스 간 통신과 동시성 제어
- Performance Optimization — 병렬 처리 적용 및 성능 비교
- Problem Solving — 문제를 재현하고 원인을 분석하여 개선

## Featured Projects

### 1. [Predictive KDS & Order Batching](https://github.com/Realangel0819/kds-order)

**주방 주문 처리 효율화를 위한 백엔드 시스템**

식당 근무 경험을 바탕으로, 같은 메뉴 주문이 개별적으로 들어올 때 발생하는 반복 조리 문제에 주목했습니다. 메뉴 조회 이벤트 처리, 서비스 간 통신, 분산락을 구현하며 주문 처리 시스템의 구조와 데이터 정합성을 학습하고 있습니다.

**Tech Stack**

[![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)](https://kafka.apache.org/)
[![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![gRPC](https://img.shields.io/badge/gRPC-244C5A?style=flat-square&logo=google&logoColor=white)](https://grpc.io/)

**주요 구현**

- Gradle 멀티모듈 기반 `order-service`, `menu-service`, `common` 구성
- gRPC와 Protocol Buffers를 활용한 서비스 간 메뉴 정보 조회
- Kafka를 활용한 메뉴 조회 이벤트 발행 및 Consumer 처리
- DynamoDB를 이용한 조회 이벤트 저장
- Redisson 기반 분산락과 Spring AOP를 활용한 동시성 제어
- 동시성 테스트에서 `Future.get()`으로 비동기 예외를 확인하고 락 대기 시간 개선

**현재 상태:** 핵심 서비스와 이벤트 파이프라인 구현 완료. 배치 그룹핑, 성능 테스트, 모니터링 및 배포 자동화를 추가 개발 중입니다.

- [소스 코드 및 실행 방법](https://github.com/Realangel0819/kds-order)
- [설계 결정 기록(ADR)](https://github.com/Realangel0819/kds-order/tree/main/docs/decisions)
- [학습 기록](https://github.com/Realangel0819/kds-order/tree/main/docs/study-log)
- [주간 회고](https://github.com/Realangel0819/kds-order/tree/main/docs/weekly-retro)

---

### 2. [Tech for Everyone](https://github.com/Capstone-Design-3rd-Team/capstone_analysis_api)

**디지털 취약계층을 위한 웹 접근성 분석 및 평가 서비스**

웹사이트 이용에 어려움을 겪는 사용자를 위해 접근성 평가 기준을 적용하고, 분석 결과와 개선 방향을 제공하는 프로젝트입니다.

**Tech Stack**

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)](https://aws.amazon.com/)

**주요 기여**

- Flask 기반 분석 서버 및 데이터 처리 흐름 구현
- 웹 크롤링이 어려운 경우를 보완하는 스크린샷 기반 분석 흐름 구성
- 이미지 분석 및 OCR 모델을 활용한 웹 요소 분석
- Docker 컨테이너 기반 분석 환경 구성
- Celery를 활용한 비동기 작업 처리 및 결과 전달 구조 구성
- AWS EC2와 S3를 활용한 서비스 배포 환경 구성

**프로젝트 결과**

- 웹 접근성 평가 결과 시각화 및 PDF 보고서 생성
- 디지털 취약계층의 웹 이용 편의성을 높이기 위한 개선 가이드 제공
- 캡스톤디자인 프로젝트 장려상 수상

- [분석 서버 소스 코드](https://github.com/Capstone-Design-3rd-Team/capstone_analysis_api)
- [캡스톤 프로젝트 팀 저장소](https://github.com/Capstone-Design-3rd-Team)

---

### 3. [SFV — Super Fast Version-Control System](https://github.com/kraftenty/sfv)

**병렬 처리를 활용한 버전 관리 시스템 성능 개선**

대용량 저장소에서 발생하는 버전 관리 작업의 처리 시간을 줄이기 위해 병렬 처리 기법을 적용하고, Git과 성능을 비교했습니다.

**Tech Stack**

[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)](https://git-scm.com/)

**성능 비교 결과**

| 작업 | Git | SFV |
| --- | ---: | ---: |
| Commit | 17.05초 | 6.39초 |
| Checkout | 5.77초 | 5.82초 |

- Commit 측정 결과 약 **62.5%의 처리 시간 단축**
- MySQL 서버 및 TensorFlow 저장소를 대상으로 성능 비교
- 대용량 파일 처리에서 병렬 처리의 효과와 한계 분석

- [SFV 소스 코드](https://github.com/kraftenty/sfv)
- [성능 측정 리포트](https://docs.google.com/document/d/1P1Ra6iWN1d6sKSznhIb1Xjiik4zfbMjt/edit?usp=sharing)

---

## Tech Stack

### Backend & Framework

[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)

### Database & Messaging

[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/)
[![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)](https://kafka.apache.org/)
[![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white)](https://aws.amazon.com/dynamodb/)

### Infrastructure & Tools

[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)](https://aws.amazon.com/)
[![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)](https://git-scm.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/)

---

## Algorithm

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=secret516)](https://solved.ac/secret516)

- [Solved.ac 프로필](https://solved.ac/secret516)
- [알고리즘 풀이 저장소](https://github.com/Realangel0819/Algorithm_Problem)

---

## Contact

- **Email:** [dlrlwk010a@gmail.com](mailto:dlrlwk010a@gmail.com)
- **Velog:** [velog.io/@realangel](https://velog.io/@realangel/posts)
- **GitHub:** [Realangel0819](https://github.com/Realangel0819)
