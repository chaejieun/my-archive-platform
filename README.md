# 📚 MyArchive (책/영화 감상 아카이빙 플랫폼)

> 개인의 책, 영화 등 콘텐츠를 검색하고 감상평을 기록하는 아카이빙 플랫폼 프로젝트

---

## 🔍 프로젝트 개요

- **목표**: 나만의 콘텐츠를 감상하고 기록할 수 있는 서비스 개발
- **주요 기능**:
  - 외부 API를 통한 콘텐츠 검색 (도서, 영화)
  - 감상평 및 별점 기록
  - 개인 콘텐츠 목록 관리 (필터, 정렬, 삭제 등)
  - (선택) 간단한 통계/시각화 기능 제공

---

## 🛠️ 기술 스택

### 📌 Frontend
- React
- MUI (Material UI)
- Axios (REST API 통신)

### 📌 Backend
- Spring Boot
- JPA (Hibernate)
- MySQL (또는 H2)
- Spring Security (JWT 인증, 추후 도입 예정)

---

## 📁 프로젝트 구조 (초기 계획)


---

## 🌐 주요 기능 정의

| 기능 | 설명 |
|------|------|
| 🔍 콘텐츠 검색 | 외부 API(Kakao Book, TMDB 등)를 활용해 검색 |
| ✍️ 감상 기록 | 별점, 메모, 감상일자 저장 |
| 📋 목록 보기 | 내가 저장한 콘텐츠들을 목록으로 조회, 정렬 |
| 💾 기록 수정/삭제 | 나의 감상 기록을 수정, 삭제 |
| ⭐ 즐겨찾기 | 즐겨찾기한 콘텐츠 목록 구분 가능 |
| 📈 (선택) 통계 | 내가 감상한 장르별 비율, 평균 별점 등 분석 제공 |

---

## 🔗 외부 API 연동 계획

| API | 설명 | 인증 |
|-----|------|------|
| Kakao Book API | 도서 검색 | REST API 키 |
| TMDB API | 영화 검색 | API 키 + Query |

---

## 🧱 DB 모델 설계 (초기)

- `User` (id, email, password, nickname)
- `Content` (id, external_id, title, type, image_url, release_date)
- `Review` (id, user_id, content_id, rating, memo, created_at)

---

## 🧪 개발 단계 및 TODO

- [x] 프로젝트 초기 세팅 (React + Spring Boot)
- [ ] 도서 검색 API 연동
- [ ] 콘텐츠 도메인 설계 및 JPA 연관관계 매핑
- [ ] 감상 기록 등록/조회/삭제 기능 구현
- [ ] 프론트: React + MUI로 기본 화면 구성
- [ ] 백엔드 연동 (Axios + REST API)
- [ ] 사용자 인증 기능 (JWT or OAuth)

---

## 🎯 목표

- 단순 CRUD를 넘어서 사용자 중심 기능 흐름 설계
- REST API 문서화 및 README 아키텍처 명확화
- 실제 배포 가능한 형태까지 구현


---

## 💬 기타

- 모든 커밋은 기능 단위로 기록 (ex. `feat: 도서 검색 기능 구현`)
- 진행 중 이슈는 `/docs/issue-log.md`에 기록 예정

