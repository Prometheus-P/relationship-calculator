# [PRD] Relationship Audit: The Loss Prevention System

**부제**: 당신의 인생 손실을 막아주는 냉혹한 회계사

- **Version**: 2.0 (The Pivot)
- **Status**: Approved for Execution
- **Target**: 2030 Emotionally Exhausted Generation & Freelancers

---

## 1. Product Vision (The Why)

**Old**: "인간관계 계산기" (재미, 가벼움, 위로)

**New**: "관계 감사(Audit) 및 손실 방지 시스템"

**Philosophy**: "시간은 돈이다. 감정 노동도 노동이다. 따라서 나쁜 관계는 '파산'이다."

**Goal**: 사용자가 모호한 감정적 고통을 **'구체적인 금전적 손실'**로 확인하고, **'손절'**이라는 합리적 의사결정을 내리도록 돕는다.

---

## 2. Core Features (The "Killer" Functions)

기존 기능을 '금융 앱'의 문법으로 재정의합니다.

### Feature 1: The Hourly Rate (시급 설정) - New & Critical

**기능**: 온보딩 시 사용자의 **'시간 가치'**를 입력받음.

> "당신의 1시간은 얼마입니까? (예: 최저시급, 내 연봉 환산액, 프리랜서 단가)"

**로직**:
- 입력된 관계 이벤트(기다림, 통화, 감정 쓰레기통)의 **'소요 시간(분)'**에 **'시급'**을 곱하여 **'비용(Cost)'**으로 자동 환산.
- **Example**: 시급 2만 원인 사용자가 친구 하소연을 30분 들어줌 → "-10,000원 손실" 즉시 기록.

### Feature 2: The Receipt of Loss (감정 영수증) - UI Overhaul

**기능**: 계산 결과 화면을 '토스/배민 영수증' 스타일로 출력.

**구성**:
- 공급가액: 실제 쓴 돈 (밥값, 술값 등)
- 부가세(VAT): 감정세 (스트레스 지수 × 가중치)
- 인건비: 투입 시간 × 시급
- **합계(Total Loss)**: "-1,450,000원" (빨간색 굵은 폰트)

**Action**: 하단에 [청구하기(공유)] 버튼 배치.

### Feature 3: The Verdict (AI 판사) - Content Upgrade

**기능**: 단순 조언이 아닌, 법원 판결문 형식의 텍스트 생성.

**Prompt Engineering (Fake or Real)**:
- "피고(상대방)는 원고(사용자)에게 심각한 금전적/정신적 피해를 입혔으므로, 즉시 '손절' 형에 처한다."
- "이 관계는 '투자 주의' 종목입니다. 비중을 축소하십시오."

---

## 3. Business Model (Monetization)

타겟을 이원화하여 수익 모델을 분리합니다.

| 구분 | Target | Product | Pricing Strategy |
|------|--------|---------|------------------|
| B2C | 연인/친구 관계 | "이별/손절 명분용 리포트" | Freemium + Ads (기본 무료, 상세 영수증 공유 시 광고 시청 or 1,000원) |
| B2B | 프리랜서/1인 기업 | "진상 클라이언트 탐지기" | SaaS Subscription (월 4,900원: 클라이언트별 ROI 대시보드 + 블랙리스트 관리) |

---

## 4. UI/UX Guidelines (The "Fin-Tech" Look)

> "이 앱은 핑크색(Love)이 아닙니다. 다크 네이비(Trust)와 레드(Warning)입니다."

- **Tone & Manner**: 냉정함, 분석적, 금융 앱 스타일.
- **Interaction**:
  - 숫자가 카운팅되는 애니메이션 (주식 잔고처럼).
  - '손절' 버튼을 누르면 문서 파쇄기 소리나 도장 찍는 소리("쾅!") 효과음.

---

## 5. Viral Strategy: "The Victim's Trophy"

> "피해자라는 사실을 가장 멋지게 증명하게 하라."

**Share Card**: 인스타그램 스토리용 1080x1920 이미지.

**Design**:
- 영수증이 길게 출력되는 모션 캡처.
- "2024년 상반기 호구 인증서: 총 손실 -500만 원" 같은 자조적인 타이틀.
- 이것이 밈(Meme)이 되어 퍼져나가게 함.

---

## 6. Implementation Roadmap (Fast Track)

### Sprint 1: The Calculator (D+1주)

- [ ] QuickLogBar 수정: '돈' 입력 필드 강조.
- [ ] '시급 설정' 기능 추가 (Local Storage 저장).
- [ ] 메인 대시보드: '감정' 대신 '손실액' 중심으로 UI 변경.

### Sprint 2: The Receipt (D+2주)

- [ ] 결과 페이지(WeeklySummaryCard 대체): 영수증 UI 디자인 및 구현.
- [ ] html-to-image 활용하여 영수증 이미지 저장 기능 구현.
- [ ] 바이럴용 카피라이팅 ("호구 탈출", "인생 구조조정") 적용.

### Sprint 3: The Verdict (D+3주)

- [ ] AI 판결 프롬프트 고도화 (B2B/B2C 분기 처리).
- [ ] B2B 구독 결제 모듈 연동 (가상).

---

## 🚀 개발자를 위한 즉시 실행 과제

가장 먼저 `src/shared/domain/report.ts`와 `src/components/dashboard` 쪽 로직을 수정해야 합니다.

1. **데이터 모델 변경**: User 모델에 `hourlyRate` (number) 필드를 추가하십시오.
2. **계산 로직 수정**: `calculateROI` 함수에서 `(timeSpent / 60) * hourlyRate`를 비용에 합산하십시오.
3. **UI 변경**: 대시보드 메인에 **"현재까지의 총 손실액: -₩000,000"**을 가장 크게 띄우십시오.

> "사람들은 조언을 듣지 않습니다. 하지만 영수증은 확인합니다."
