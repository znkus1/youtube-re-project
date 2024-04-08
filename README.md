# YouTube 추천 알고리즘 리버스 엔지니어링 [[project-link]](https://github.com/orgs/yeardream-final-project-06team/repositories))

## 프로젝트 개요
- **프로젝트 한 줄 설명:**
    - 유튜브 추천 알고리즘 리버스 엔지니어링을 위한 크롤링 아키텍처 개발 및 데이터 파이프라인 구축
    - 페르소나 생성하여 페르소나가 시청한 영상 데이터를 분석하여 유튜브 추천 알고리즘을 분석
- **프로젝트 배경 또는 기획 의도:**
    - 유튜브 페르소나의 행동 데이터를 기반으로 타겟을 분석하여 제시함으로써, 광고주들에게 실질적인 인사이트를 제공하며 광고의 효율성을 높일 수 있는 마케팅 전략 수립에 도움이 될 수 있도록 함이 목적
- **팀 프로젝트:** 4인
- **팀 프로젝트 참여 인원 및 본인 역할:**
    - ELK Stack을 활용한 데이터 파이프라인 구축
    - 대시보드 구성
- **진행 기간 및 소속:**
    - 2023.11.06 - 2023.12.16 (6주)

## 기술 스택 및 데이터셋 설명

- **활용 기술 스택:**
    - AWS EC2, Python, Selenium, Tor, Elasticsearch, Logstash, Kibana, FastAPI, MongoDB, Docker, Docker Swarm
- **데이터 출처, 용량, 특징:**
    - 약 100개의 임의의 페르소나와 해당되는 키워드
    - YouTube 크롤링을 통해서 약 40만개의 데이터 수집
      
![architecture](https://github.com/znkus1/final-project/assets/130662133/8d3f4bf3-1067-463b-85ff-598662ff6846)

## 프로젝트 진행 단계

1. **크롤러 개발**
2. **데이터 파이프라인 구축**
3. **데이터 분석**
4. **데이터 시각화**

## 프로젝트 세부 과정

- **크롤링 아키텍처 개발:**
    - Python기반 크롤러 개발 (Selenium과 Tor를 활용)
    - FastAPI, MongoDB 활용하여 페르소나 관리 및 키워드 랜덤 추출
    - Docker-Swarm 클러스터 구축
- **데이터 파이프라인 구축:**
    - Logstash를 활용해 크롤링, 로그 데이터 수집
    - Elasticsearch 크롤링 데이터 저장
- **데이터 분석:**
    - TF-IDF
    - 코사인 유사도 판단 -> 선택한 영상과 유사한 영상제시
- **데이터 시각화:**
    - Kibana를 이용해 대시보드
<img width="1716" alt="Untitled" src="https://github.com/znkus1/final-project/assets/130662133/3950c465-4bb9-4ac6-971b-8f267cdd6c2c">

## 프로젝트 회고

- **잘 한점:**
    - 디스코드를 이용해서 크롤링 작업 중에 도커 컨테이너 오류 상황시에 알림을 발송하여 실시간으로 확인할 수 있도록 처리하였음
- **한계점 및 개선 방안:**
    - 데이터 분석 부분에서 관련 지식이 부족하여 추천 알고리즘 모델을 개발하는 단계까지 도달하지 못함
    - 예산상의 이유로 쿠버네티스 클러스터를 구축하지 못하여 대신 도커 스웜으로 클러스터 구축
