# SpendWise 💸
**Flutter + FastAPI 기반 소비 관리 및 분석 어플리케이션**

---

## 📱 프로젝트 개요

> SpendWise는 개인 소비 습관을 시각화하고, 카테고리별 소비 분석 및 목표 설정을 통해 지출을 효율적으로 관리할 수 있도록 도와주는 앱입니다.

- Flutter 기반 모바일 클라이언트
- FastAPI 기반 RESTful 백엔드 서버
- JWT 기반 사용자 인증 및 보호된 API
- 소비 데이터를 활용한 AI 예측 및 분석 기능 구현

---

## 🚀 핵심 기능

| 기능 | 설명 |
|------|------|
| ✅ 회원가입 / 로그인 | JWT 토큰 기반 인증 및 사용자 보호 |
| ✅ 소비 내역 등록 및 조회 | 날짜, 카테고리, 메모, 금액 등 기록 |
| ✅ 소비 분석 (월별/카테고리별) | Pie Chart 기반 소비 분포 시각화 |
| ✅ 소비 목표 설정 | 월 단위 목표 설정 및 초과 여부 확인 |
| ✅ 캘린더 시각화 | 날짜별 총 소비 금액에 따라 색상 표시 |
| 🧠 소비 예측 (AI) | 다음 달 예상 소비 금액 및 가장 많이 소비할 분야 예측 (예: "식비가 현재 추세라면 50만 원을 초과할 수 있어요") |
| 💡 소비 습관 개선 피드백 (AI) | 소비 패턴 분석 후 절약 팁 및 사용자 맞춤 피드백 제공 (예: "교통비는 평균보다 낮습니다. 좋은 소비 습관이에요") |

---

## 🛠️ 기술 스택

### 📦 Frontend (Flutter)
- `flutter`, `http`, `provider`
- `table_calendar`: 캘린더 UI 위젯 활용
- `fl_chart`: 카테고리별 소비 원형 차트 시각화

### 🔧 Backend (FastAPI)
- FastAPI, MySQL, PyJWT
- RESTful API 설계 및 문서화 (`Swagger UI`)
- OAuth2PasswordBearer + JWT 기반 인증 구현
- 사용자별 소비 데이터 집계 SQL (일/월 단위)

### 🤖 AI 소비 예측 및 피드백 로직
- **입력 데이터**: 사용자 ID별 날짜, 금액, 카테고리
- **AI 처리 흐름**:
    - 소비 기록을 월별로 집계 → 회귀 분석 기반 예측
    - 평균 대비 소비 패턴 비교 → 자연어 피드백 제공
- **예측 예시**:
    - "이번 추세라면 다음 달 식비가 50만 원을 초과할 수 있어요"
    - "교통비는 평균보다 낮습니다. 좋은 소비 습관이에요"

---

## 📷 시연 이미지

> 주요 화면 구성 및 기능 흐름

### 📌 소비 내역 캘린더 (목표 초과 시 경고 표시)

<img src="assets/screens/calendar_warning.png" width="400"/>

- 날짜별 소비 기록이 캘린더에 시각화되어 표시되며, 총 금액에 따라 색상이 구분됩니다.
- 사용자가 설정한 소비 목표를 초과할 경우 자동 경고 팝업이 표시됩니다.

---

### 📌 소비 내역 등록 화면

<img src="assets/screens/entry_form.png" width="300"/>

- 카테고리, 금액, 메모, 날짜를 선택하여 소비 내역을 쉽게 기록할 수 있습니다.

---

### 📌 소비 분석 및 AI 예측 결과 화면

<img src="assets/screens/analysis_ai.png" width="400"/>

- 월간 소비 내역을 카테고리별로 분류하여 파이차트로 시각화합니다.
- AI가 다음 달 소비를 예측하고, 예상 초과 지출 카테고리를 분석하여 피드백을 제공합니다.

---

### 📌 소비 내역 캘린더 UX (GIF)

<img src="assets/screens/calendar_demo.gif" width="300"/>

- 날짜 선택 시 해당일 소비 내역이 상세히 표시되며, 카테고리별 금액까지 확인 가능합니다.
- 달력은 시각적으로 직관적이며, 일일 총 소비 금액도 함께 표시됩니다.




---

## 🧠 개발 포인트 & 회고

- Flutter ↔ FastAPI 연동 구조 설계 및 JWT 인증 적용
- FastAPI에서 사용자별 소비 데이터 집계 및 통계 API 설계
- SQL 기반 날짜별/카테고리별 소비 통계 쿼리 최적화
- 소비 데이터 기반 분석 결과를 사용자 피드백으로 자연스럽게 연동
- 차후 GPT 기반 자연어 소비 설명 및 예측 고도화 예정

---

## 🏁 실행 방법

### ✅ Backend

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