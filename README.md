# 한대성 (Daniel Han) — Data Engineer

> **"데이터 파이프라인으로 비즈니스 문제를 0 to 1로 해결합니다."**

12년 차 Full-Stack 경력 기반 **데이터 엔지니어**  
금융·물류·커머스·보안 등 다양한 도메인에서 시스템을 직접 설계·운영한 경험을 바탕으로,  
**데이터 파이프라인 구축**, **AI 서비스 인프라**, **배치·실시간 ETL 자동화**에 집중하고 있습니다.

---

## 🧠 About Me

- 🏆 데이터 엔지니어 부트캠프 **최우수상** 수상
- ⚙️ Airflow · Spark · Kafka · Hadoop HDFS **엔드-투-엔드 데이터 파이프라인** 완전 자동화
- 🔍 Elasticsearch 기반 **검색 인덱싱 파이프라인** 설계·구축 경험
- 🐳 Docker 14컨테이너 · GitHub Actions CI/CD · AWS GPU 서버(NVIDIA T4) · GCP 운영 경험
- 🤖 YOLOv11 · Fashion-CLIP · LLaVA · SBERT **AI 모델 서빙 인프라** 구축
- 💼 12년 Full-Stack 경력 (금융·물류·커머스·보안 도메인) — 비즈니스 로직과 데이터 흐름을 함께 이해하는 엔지니어

---

## 🛠️ Tech Stack

| 영역 | 기술 |
|------|------|
| **Data Pipeline** | Apache Airflow, Apache Spark, Hadoop HDFS, Apache Kafka |
| **Database** | PostgreSQL, MongoDB, MySQL, Redis, Oracle, MariaDB |
| **Search & Vector DB** | Elasticsearch (KNN 벡터 검색, 이중 인덱스 설계) |
| **Cloud & DevOps** | AWS, GCP, Docker, GitHub Actions, Jenkins |
| **Backend** | Python, FastAPI, Java, Spring Boot, Node.js |
| **AI/ML** | YOLOv11, Fashion-CLIP, SBERT, LLaVA |
| **Frontend** | Vue.js, JavaScript, HTML/CSS |

---

## 🚀 Featured Projects

### 🧴 PickSafe — 화장품 성분 알레르기 스캔 PWA

| 외국인 관광객을 위한 실시간 화장품 전성분 OCR 스캔 및 알레르기·기피 성분 맞춤 대조 PWA

- **역할**: 1인 개발 (기획·설계·풀스택 개발·인프라 운영 100%)
- **파이프라인**: 카메라 촬영 / 화면 캡처 이미지 붙여넣기 → Gemini Vision OCR(텍스트 추출) → 4단계 성분 매칭 엔진(Exact → Normalized → Fuzzy Levenshtein → Token Split, 4.9만 건 마스터) → 개인 맞춤 기피·공인 알레르겐 대조
- **안정성 설계**: Neon Postgres 85% 쿼터 사전 경고 및 2-Phase(Bulk UPSERT + In-flight Catch-up) 동기화 기반 자동 핫스왑 페일오버 설계, 512MB RAM 제약 대응 서킷 브레이커로 OOM 방지
- **인프라 & 성능**: Gemini API 멀티 계정 로드밸런싱, Cloudflare 엣지 캐싱, 다국어 사전 In-Memory 2-Tier 캐싱으로 템플릿 N+1 쿼리 병목 해소
- **글로벌 & UX**: 글로벌 7개 국어(한국어·영어·일본어·중국어 간/번체·포르투갈어·튀르키예어) 지원 (정적 감사 결측 0건 검증), 비로그인 무제한 게스트 모드, 모바일 웹 PWA 환경
- **Stack**: `Python` `FastAPI` `PostgreSQL(Neon)` `Gemini API` `Jinja2` `Vanilla JS` `PWA` `Cloudflare` `Render`
- 🌐 [서비스 바로가기](https://picksafe.kr)

---

### 👕 LOOKALIKE — AI 패션 이미지 검색 플랫폼 🏆 최우수상
> 듀프(Dupe) 소비 트렌드를 겨냥한 AI 패션 이미지 검색 + 실시간 최저가 비교 서비스

- **역할**: Lead DE · Pipeline Architect · 팀장 (4인 팀)
- **파이프라인**: Airflow DAG → 5개 브랜드 크롤링 → Hadoop HDFS → Spark ETL → AI 임베딩 → Elasticsearch KNN 인덱싱
- **AI 검색**: YOLOv11 세그멘테이션 + Fashion-CLIP(이미지) / LLaVA VLM + SBERT(텍스트) 이중 벡터 Late Fusion
- **모니터링**: Kafka 기반 실시간 메트릭 스트리밍, Auto-Recovery, Slack 알람
- **인프라**: AWS EC2 g4dn.xlarge (NVIDIA T4 GPU), GCP, Docker Compose 14개 서비스, GitHub Actions CI/CD
- **Stack**: `Python` `Airflow` `Spark` `Kafka` `Elasticsearch` `PostgreSQL` `MongoDB` `Docker` `AWS`
- 🌐 [서비스 바로가기](https://lookalike-api.onrender.com)

---

### 💄 OliveYoung Backoffice Remodel
> 올리브영 매장 백오피스 시스템 기능 개선 및 리모델링

- Nexacro → Vue + SpringBoot 환경 전환으로 라이선스 비용 절감
- 테스터·라벨 등록 관리 페이지 개발, 사용자 만족도 20% 향상
- **Stack**: `Java` `SpringBoot` `Vue.js` `AG-grid` `Oracle` `DataDog`

---

### 📦 글로벌 물류 API 연동 시스템
> 미국·일본·동남아 배송 통합 물류 솔루션

- UPS/DHL API 연동 리드, Order·Label·Tracking 전체 서비스 구축
- OPEN API 구축으로 고객사 실무자 능률 80% 향상, 물류 계약 건 25% 증가
- **Stack**: `Java` `Spring Boot` `Vue.js` `Vuetify` `MariaDB` `AWS` `MSA`

---

### 💻 Portfolio Management Site(Personal Project)
> Supabase + Vercel 기반 개인 이력 관리 웹사이트

- 이력서, 경력기술서, 프로젝트 상세페이지, 방문자 분석 대시보드
- **Stack**: `Next.js` `Supabase` `Vercel` `Render`
- 🌐 [바로가기](https://daniel-profile-site.vercel.app)

---

## 📈 GitHub Stats

![Daniel's GitHub stats](https://daniel-stats.vercel.app/api?username=daniel-dataflow&show_icons=true&theme=react&cache_seconds=300)
![Top Langs](https://daniel-stats.vercel.app/api/top-langs/?username=daniel-dataflow&layout=compact&theme=react&hide=jupyter%20notebook,html)

---

## 📫 Contact

| | |
|---|---|
| 🌐 Portfolio | [daniel-profile-site.vercel.app](https://daniel-profile-site.vercel.app) |
| ✉️ Email | daniel.han.developer@gmail.com |
| 💼 LinkedIn | [linkedin.com/in/danielhan-](https://www.linkedin.com/in/danielhan-/) |
