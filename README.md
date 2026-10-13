 <div align="center">
  <img src="https://capsule-render.vercel.app/api?type=cylinder&color=ca99d5&height=180&text=AlwaysNight&fontColor=ffffff&fontSize=60" />
</div>

<div align="center">
  <h2>꾸준히 고민하고, 직접 검증하는 개발자</h2>
  <p>문제를 분석하고 해결 과정을 코드와 실험으로 증명합니다.</p>
  <p>
    <a href="https://github.com/Realangel0819">GitHub</a> ·
    <a href="https://velog.io/@realangel/posts">Velog</a> ·
    <a href="mailto:dlrlwk010a@gmail.com">Email</a>
  </p>
</div>

---

## About Me

- 문제의 원인을 분석하고, 여러 해결 방법을 비교해 적절한 방식을 선택합니다.
- 동시성, 비동기 처리, 서비스 간 통신 등 백엔드의 핵심 문제를 프로젝트로 학습합니다.
- 구현에 그치지 않고 테스트와 실험을 통해 결과를 검증하려고 노력합니다.
- 새로운 기술을 학습할 때 동작 원리와 설계 이유를 이해하는 것을 중요하게 생각합니다.

## Featured Projects

### 1. Predictive KDS & Order Batching

**주방 주문 시스템 백엔드**

[Repository](https://github.com/Realangel0819/kds-order)

주방에서 같은 메뉴의 주문이 몰릴 때 발생하는 반복 조리 문제를 줄이기 위해 시작한 백엔드 프로젝트입니다.

**Tech Stack**

`Java 17` `Spring Boot` `Gradle` `MySQL` `Kafka` `Redis` `Redisson` `gRPC` `DynamoDB`

**주요 구현 및 문제 해결**

- Gradle 멀티모듈 구조로 `order-service`, `menu-service`, `common` 모듈 분리
- gRPC와 Protocol Buffers를 활용한 서비스 간 메뉴 정보 조회
- Kafka 기반 메뉴 조회 이벤트 발행 및 DynamoDB 적재
- Redisson 분산 락과 Spring 트랜잭션 실행 순서를 조정해 동시성 문제 해결
- `Future.get()`으로 비동기 작업의 예외를 확인하고, 락 대기 시간 부족으로 발생한 요청 누락 원인 분석
- Kafka의 Zookeeper 의존성을 제거하고 KRaft 모드로 전환해 컨테이너 연결 장애 해결

**검증 결과**

100건의 동시 요청 테스트에서 메뉴별 주문 건수가 요청 수와 일치하는 것을 확인했습니다.

### 2. Web Accessibility Evaluation Tool

**디지털 취약계층을 위한 웹사이트 접근성 평가 서비스**

[AI 분석 API Repository](https://github.com/Capstone-Design-3rd-Team/capstone_analysis_api)

웹사이트의 접근성 문제를 분석해 사용자가 더 쉽게 이용할 수 있도록 돕는 캡스톤 프로젝트입니다.

**Tech Stack**

`Python` `Flask` `Docker` `OCR` `Celery` `AWS EC2` `AWS S3`

**주요 구현 및 문제 해결**

- 웹사이트 크롤링을 통한 화면 요소 수집
- 크롤링이 차단된 사이트를 보완하기 위한 화면 캡처 및 OCR 기반 요소 추출
- UI 인식 및 OCR에 사용하는 AI 모델의 Docker 이미지 패키징
- 무거운 이미지 분석 작업을 비동기로 처리하도록 작업 큐 기반 구조 구성
- 백엔드와 협의해 대용량 데이터를 한 번에 전달하는 대신 작업 완료 후 결과를 콜백으로 전달하는 방식 적용
- AWS EC2와 S3를 활용한 서비스 배포

프로젝트를 통해 크롤링 실패에 대응하는 대체 처리 경로를 구현하고, 서버의 작업 부담을 분산하는 경험을 쌓았습니다.

### 3. SFV — Super Fast Version-Control-System

**병렬 처리를 활용한 버전 관리 시스템**

[Repository](https://github.com/kraftenty/sfv)

대용량 저장소의 버전 관리 시간을 줄이기 위해 여러 병렬 처리 방식을 구현하고 Git과 성능을 비교한 팀 프로젝트입니다.

**Tech Stack**

`Java` `Multithreading` `parallelStream` `Producer-Consumer`

**주요 구현 및 검증**

- 변경 파일 탐지, 커밋, 체크아웃 작업 구현
- 단일 처리, `parallelStream`, 청크 분배 방식의 성능 비교
- 생산자-소비자 구조를 적용한 체크아웃 작업 분배 개선
- MySQL Server 및 TensorFlow 저장소를 대상으로 성능 측정

**측정 결과**

| 작업 | Git | SFV |
|---|---:|---:|
| Commit | 17.05초 | 6.39초 |
| Checkout | 5.77초 | 5.82초 |

커밋 처리 시간은 Git 대비 약 62.52% 단축했습니다. 체크아웃은 Git과 비슷한 성능을 보였으며, 저장소 특성에 따른 최적화의 한계도 확인했습니다.

---

## Tech Stack

### Backend
<p>
  <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white" />
</p>

### Database & Messaging
<p>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon_DynamoDB-4053D6?style=for-the-badge&logo=amazondynamodb&logoColor=white" />
  <img src="https://img.shields.io/badge/gRPC-244C5A?style=for-the-badge&logo=google&logoColor=white" />
</p>

### AI & Infrastructure
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white" />
</p>

### Languages & Tools
<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</p>

## Problem Solving

<div align="center">
  <a href="https://solved.ac/secret516">
    <img src="http://mazassumnida.wtf/api/v2/generate_badge?boj=secret516" alt="Solved.ac Profile" />
  </a>
</div>

## Contact

<div align="center">
  <a href="mailto:dlrlwk010a@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://velog.io/@realangel/posts">
    <img src="https://img.shields.io/badge/Velog-20C997?style=for-the-badge&logo=velog&logoColor=white" />
  </a>
  <a href="https://github.com/Realangel0819">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</div>
