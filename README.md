# SpendWise 💸
**Flutter + FastAPI 기반 소비 관리 및 분석 애플리케이션**

---

## 📱 프로젝트 개요

> SpendWise는 사용자의 소비 습관을 시각화하고, 카테고리별 분석 및 목표 설정을 통해 효율적인 지출 관리를 지원하는 통합 소비 분석 플랫폼입니다.

- Flutter 기반 모바일 클라이언트
- FastAPI 기반 RESTful 백엔드 서버
- JWT 인증 기반 보안 API 설계
- 소비 패턴 기반 AI 예측 및 개인 맞춤 피드백 제공

---

## 🚀 핵심 기능

| 기능 | 설명 |
|------|------|
| ✅ 회원가입 / 로그인 | JWT 기반 사용자 인증 및 보안 |
| ✅ 소비 내역 등록 및 조회 | 날짜, 카테고리, 금액, 메모 입력 및 확인 |
| ✅ 소비 분석 (월별/카테고리별) | 파이 차트 기반 소비 분포 시각화 |
| ✅ 소비 목표 설정 | 월별 목표 금액 설정 및 초과 시 경고 알림 |
| ✅ 캘린더 시각화 | 일자별 총 소비 금액을 색상으로 표현 |
| 🧠 소비 예측 (AI) | 다음 달 예상 소비 금액 및 주요 소비 카테고리 예측 |
| 💡 소비 습관 피드백 (AI) | 사용자 소비 성향에 기반한 절약 팁 제공 |

---

## 🛠️ 기술 스택

### 📦 Frontend (Flutter)
- `flutter`, `http`, `provider`
- `table_calendar`: 캘린더 UI 구성
- `fl_chart`: 카테고리별 소비 시각화

### 🔧 Backend (FastAPI)
- FastAPI, MySQL, PyJWT
- OAuth2PasswordBearer 기반 JWT 인증
- Swagger UI 기반 API 문서화
- SQL 집계 기반 통계 및 분석 API

### 🤖 AI 기반 소비 예측 및 피드백 로직
- **데이터 입력**: 사용자별 날짜, 카테고리, 금액
- **AI 흐름**:
    - 월간 소비 집계 → 회귀 모델 기반 예측
    - 평균과의 소비 비교 → 자연어 기반 피드백 생성
- **예시 출력**:
    - “현재 추세라면 다음 달 식비가 50만 원을 초과할 수 있어요.”
    - “교통비는 평균보다 낮습니다. 좋은 소비 습관이에요.”

---

## 📷 주요 화면 구성

> UI 미리보기 및 기능 흐름 예시

### 📌 소비 내역 캘린더 (소비 금액 시각화)

<img src="https://github.com/user-attachments/assets/ef51bd4c-fdef-4a48-accd-083eabe6dc91" height="400" />

- 각 날짜별 소비 금액에 따라 신호등 색상으로 표시됩니다.

---

### 📌 소비 목표 설정 및 초과 알림

<img src="https://github.com/user-attachments/assets/36e88d12-cd8f-4bae-aa97-d194206bc593" height="400" />
<img src="https://github.com/user-attachments/assets/fa2d5da4-a5f3-45f5-88af-82429885f118" height="400" />

- 사용자는 월간 소비 목표를 설정할 수 있으며, 초과 시 시각적 경고가 표시됩니다.

---

### 📌 소비 내역 등록 화면

<img src="https://github.com/user-attachments/assets/6bbc6248-ffeb-489a-94f9-70204b82feae" height="400" />
<img src="https://github.com/user-attachments/assets/12141424-d308-4305-96ca-992ab70e9a7e" height="400" />

- 카테고리, 금액, 메모, 날짜를 선택하여 간편하게 소비 내역을 등록할 수 있습니다.

---

### 📌 소비 분석 및 AI 예측 결과

<img src="https://github.com/user-attachments/assets/c820aa53-32f5-4c72-923c-865bb8b52a0e" height="400" />

- 월별 소비를 카테고리 기준으로 분석하고, AI 기반 소비 예측과 피드백을 제공합니다.

---

### 📌 앱 시연 UX (GIF)

<img src="https://github.com/user-attachments/assets/35c37fd1-0999-471d-ab89-a945e4655195" height="400" />

---

## 🧠 개발 포인트 & 회고

- Flutter ↔ FastAPI 연동 구조 및 JWT 인증 설계
- 사용자별 소비 데이터를 기반으로 한 통계 집계 쿼리 최적화
- 자연스러운 피드백 UX 구현을 위한 분석 → 텍스트 변환 구조 설계
- 추후 GPT 기반 자연어 설명 및 예측 기능 고도화 예정

---

## 🏁 실행 방법

### ✅ Backend 실행

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

### ✅ Frontend

```bash
cd frontend
flutter pub get
flutter run


 개발자
이름: 박시연

GitHub: @siyeoncoding
