# Ep 8: 반전의 단서

**구산구 AI 혁명기 - Episode 8**

---

## 소설 본문

![구산구청 복지정책과 - 새벽 2시](placeholder)

새벽 2시. 구산구청 복지정책과. 민준, 박소희, 윤서연 인턴, 그리고 김철수가 모여 있었다.

민준은 화이트보드에 계획을 적었다.

```
[목표] 허위 제보 반박 + 검증 시스템 구축

1단계: 김영수 씨 실존 여부 확인
2단계: AI 판단 과정 투명화
3단계: 오류 방지 시스템 제시
```

김철수가 손을 들었다.

"민준 씨, 그런데 김영수 씨가 실존 인물인지 어떻게 확인해요?"

"주민등록 전산망 조회해야죠."

"그건 민원실에 권한 있어요. 우린 못 해요."

민준은 입술을 깨물었다.

박소희가 나섰다.

"내가 민원실 과장한테 부탁해볼게요. 새벽이지만..."

10분 후. 민원실 과장이 전화로 답했다.

"박 과장, 확인했어요. 김영수, 1951년생, 구산구 거주... 2024년 3월 18일 사망 신고 접수됐어요."

민준은 화이트보드에 적었다.

```
김영수: 실존 인물 (사망 2024.03.18)
→ 우리 명단에 없음 (Never selected by AI)
→ 허위 제보 확정
```

"좋아요. 1단계 완료. 이제 2단계..."

윤서연이 일어섰다.

"주무관님, 제가 Custom GPT 만들어볼게요."

"Custom GPT?"

"네. 구산구 전용 복지 검증 봇이요."

---

![구산구청 복지정책과 - 새벽 3시, 윤서연의 작업](placeholder)

윤서연은 노트북을 열고 ChatGPT Plus에 접속했다.

"Custom GPT는... ChatGPT를 특정 목적에 맞게 커스터마이징하는 거예요."

민준이 물었다.

"어떻게 만드는데요?"

"간단해요. ChatGPT한테 '이런 봇 만들어줘'라고 하면, ChatGPT가 알아서 설정을 만들어줘요."

윤서연은 타이핑을 시작했다.

```
너는 GPT Builder야.
아래 요구사항에 맞는 Custom GPT를 설계해줘.

[봇 이름] 구산구 복지 검증 봇

[목적]
복지 대상자 명단을 분석하고, 오류 가능성이 있는 케이스를 사전에 필터링

[입력]
- 이름, 나이, 독거 여부, 최근 연락일, 주소

[출력]
1. 우선순위 (1~10점)
2. 재확인 필요 여부 (⚠️ 플래그)
3. 판단 근거 (투명성)

[재확인 필요 조건]
- 연락 두절 3개월 이상
- 80세 이상 독거 노인
- 주소 불명확

[추가 기능]
- 판단 과정을 단계별로 설명
- 사람이 최종 확인할 항목 명시
```

엔터. 10초 후.

```
[GPT Builder 응답]
Custom GPT 설정을 생성했습니다.

[봇 이름] 구산구 복지 검증 봇

[Instructions]
You are a welfare verification assistant for Gusan-gu municipal office.
Analyze welfare recipient candidates and flag cases requiring human verification.
Always explain your reasoning step-by-step for transparency.
...

[Conversation Starters]
- 이 명단을 분석해주세요
- 재확인이 필요한 케이스를 찾아주세요
- 우선순위를 정해주세요
```

윤서연은 "Create" 버튼을 눌렀다.

"완성!"

민준은 화면을 봤다. '구산구 복지 검증 봇'이 생성되어 있었다.

"이제 테스트해볼게요."

---

![구산구청 복지정책과 - 새벽 4시, 테스트](placeholder)

윤서연은 테스트 데이터를 입력했다.

```
[명단]
이름, 나이, 독거, 최근연락, 주소
이순자, 78, 독거, 2024-06-01, 구산구 행복동 123
김영수, 73, 독거, 2024-03-15, 구산구 희망동 456
박철수, 65, 동거, 2024-05-20, 구산구 사랑동 789
```

봇이 분석을 시작했다.

```
[분석 결과]

1. 이순자 (78세)
   우선순위: 8점
   ⚠️ 재확인 필요: 고령 독거
   판단 근거:
   - 최근 연락일: 1주일 전 (정상)
   - 고령 독거 → 정기 확인 필요
   
2. 김영수 (73세)
   우선순위: 9점
   ⚠️⚠️ 긴급 재확인 필요
   판단 근거:
   - 최근 연락일: 3개월 전 (위험)
   - 독거 노인 → 사망/입원 가능성
   - **주민등록 확인 필수**
   
3. 박철수 (65세)
   우선순위: 5점
   재확인 불필요
   판단 근거:
   - 최근 연락일: 2주 전 (정상)
   - 동거 → 상대적 안전
```

민준은 숨을 멈췄다.

"이거... 김영수 씨를 자동으로 걸러내네요?"

"네. '주민등록 확인 필수'라고 플래그를 달았어요."

박소희가 화면을 봤다.

"윤 인턴, 이게 진짜 작동해요?"

"네, 과장님. 이제 이걸 전 직원이 쓰게 하면, 김영수 씨 같은 케이스는 자동으로 걸러져요."

김철수가 감탄했다.

"와... 이거 진짜 대단한데?"

민준은 고개를 끄덕였다.

"좋아요. 이제 3단계. 기자회견 준비해요."

---

![구산구청 브리핑룸 - 오전 10시](placeholder)

오전 10시. 구산구청 브리핑룸. 20명의 기자들이 모였다. 카메라가 민준을 향했다.

최태양 국장이 먼저 발언했다.

"어제 보도된 '구산구청 AI 오류' 건에 대해 해명드리겠습니다."

"먼저, 김영수 씨는 우리 복지 대상자 명단에 포함된 적이 없습니다. 허위 제보입니다."

기자가 손을 들었다.

"증거는요?"

민준이 일어섰다.

"제가 설명드리겠습니다."

민준은 노트북을 프로젝터에 연결했다. 화면에 엑셀 파일이 떴다.

"이건 우리 복지 대상자 명단입니다. 총 150명. 김영수 씨는 없습니다."

"Ctrl+F로 검색해보시죠."

민준은 실시간으로 '김영수'를 검색했다. 0건.

"보시다시피, 없습니다."

기자가 재차 물었다.

"그럼 어제 공문은 위조인가요?"

"네. 누군가 우리 양식을 도용해 만든 겁니다."

"누가요?"

민준은 잠시 침묵했다.

"...현재 수사를 의뢰한 상태입니다."

또 다른 기자가 손을 들었다.

"하지만 AI가 실수할 가능성은 있잖아요? 앞으로 어떻게 방지할 건가요?"

민준은 고개를 끄덕였다.

"좋은 질문입니다. 그래서 저희가 새로운 시스템을 만들었습니다."

---

![구산구청 브리핑룸 - Custom GPT 시연](placeholder)

민준은 화면을 전환했다. 'Custom GPT: 구산구 복지 검증 봇'이 떴다.

"이건 우리가 개발한 검증 전용 AI입니다."

"기존 AI는 우선순위만 정했다면, 이 봇은 오류 가능성까지 체크합니다."

민준은 실시간으로 테스트 데이터를 입력했다. 김영수 씨 포함.

봇이 분석했다.

```
김영수 (73세)
⚠️⚠️ 긴급 재확인 필요
이유: 연락 두절 3개월
→ **주민등록 확인 필수**
```

"보시다시피, 이 봇은 '연락 두절 3개월 이상'인 케이스를 자동으로 플래그합니다."

"그리고 '주민등록 확인 필수'라고 사람에게 알려줍니다."

"즉, AI 판단 + 사람 확인 = 이중 검증입니다."

기자들이 수군거렸다.

"이거... 다른 지자체도 쓸 수 있나요?"

민준은 웃었다.

"네. 오픈소스로 공개할 예정입니다."

---

![구산구청 앞 - 주민 서명 운동](placeholder)

오후 2시. 구산구청 앞. 주민 50명이 모였다.

이순자 할머니가 앞에 섰다.

"저는 구산구에 50년 살았어요. 구청이 저를 찾아준 덕분에 지금 살아 있어요."

"민준 주무관님 잘못 없어요. 누군가 거짓말한 거예요."

주민들이 박수 쳤다.

"강민준 주무관 응원합니다!"

"구산구청 AI 계속 써주세요!"

서명지에 이름이 채워졌다. 100명, 200명... 500명.

---

![구산구청 복지정책과 - 오후](placeholder)

오후 5시. 민준은 뉴스를 확인했다.

```
[속보] 구산구청, Custom GPT로 AI 오류 방지 시스템 구축
"투명성과 검증, 두 마리 토끼 잡았다"

구산구청이 AI 오류 논란에 대해 혁신적인 해법을 제시했다.
Custom GPT를 활용한 검증 시스템으로, AI 판단 과정을 투명하게 공개하고
오류 가능성을 사전에 차단한다는 전략이다.
```

댓글이 바뀌었다.

```
"구산구 진짜 혁신하네"
"이제 다른 구청들도 따라 해야지"
"처음부터 이렇게 했어야지 ㅋㅋ"
"강민준 주무관 응원합니다"
```

박소희가 다가왔다.

"민준 씨, 봤어요? 여론 완전히 역전됐어요."

"네... 믿기지 않아요."

최태양 국장이 들어왔다.

"강 주무관, 박 과장, 윤 인턴, 김 주무관. 고생 많았어요."

최태양은 민준의 어깨를 두드렸다.

"민준 씨, 청담구로 돌아가고 싶어요?"

민준은 고개를 저었다.

"아니요. 여기 아직 할 일이 많아요."

박소희가 웃었다.

"민준 씨, 이제 진짜 구산구 사람 됐네요."

---

## 💡 Tutorial: Custom GPT 만들기

**민준과 윤서연이 사용한 기술: 맞춤형 AI 봇 개발**

### 1. Logic (원리)

**문제 상황:**
- 일반 ChatGPT는 범용적 (모든 걸 할 수 있지만, 전문성 부족)
- 매번 긴 프롬프트 반복 입력 (비효율)
- 조직 내 여러 사람이 쓸 때 일관성 부족

**Custom GPT란?**
- ChatGPT를 **특정 업무에 특화**시킨 봇
- 프롬프트를 **미리 설정**해서 누구나 쉽게 사용
- **지식 파일 업로드** 가능 (조례, 매뉴얼 등)

**비유:**
- 일반 ChatGPT = 만능 비서
- Custom GPT = 복지 전담 비서 (복지만 전문)

### 2. Stack (도구)

**필요 조건:**
- ChatGPT Plus (유료, 월 $20)
- 또는 ChatGPT Team/Enterprise

**접속 방법:**
1. ChatGPT 접속
2. 왼쪽 사이드바 "Explore GPTs" 클릭
3. 우측 상단 "Create" 버튼 클릭

### 3. Guide (실행)

#### Step 1: GPT Builder와 대화하기

**가장 쉬운 방법:**

ChatGPT에게 **"내가 원하는 봇"**을 설명하면, ChatGPT가 알아서 만들어줍니다.

```
Create a Custom GPT for me.

[Purpose]
Help municipal office staff verify welfare recipient candidates

[Input]
Name, age, living situation, last contact date

[Output]
Priority score (1-10)
Flag for cases requiring human verification
Reasoning for transparency

[Special Rules]
- Flag if no contact for 3+ months
- Flag if age 80+ and living alone
- Always explain step-by-step
```

GPT Builder가 자동으로 설정을 생성합니다.

#### Step 2: 설정 확인 및 수정

**Configure 탭에서 확인:**

**1) Name (봇 이름):**
```
구산구 복지 검증 봇
```

**2) Description (설명):**
```
복지 대상자 명단을 분석하고 재확인이 필요한 케이스를 자동으로 플래그합니다.
```

**3) Instructions (핵심 지시사항):**
```
You are a welfare verification assistant for Gusan-gu.

Your job:
1. Analyze welfare recipient candidates
2. Assign priority scores (1-10)
3. Flag cases requiring human verification

Flag criteria:
- No contact for 3+ months: ⚠️⚠️
- Age 80+ and living alone: ⚠️
- Unclear address: ⚠️

Always explain your reasoning step-by-step for transparency.
```

**4) Conversation Starters (시작 질문):**
```
- 이 명단을 분석해주세요
- 재확인이 필요한 케이스를 찾아주세요
- 김영수 씨를 검증해주세요
```

**5) Knowledge (지식 파일 업로드):**
```
- 구산구 복지 업무 매뉴얼.pdf
- 복지 대상자 선정 기준.docx
```

#### Step 3: 테스트

**Preview 탭에서 실시간 테스트:**

```
[사용자]
이 명단을 분석해주세요.

이름: 이순자, 나이: 78, 독거, 최근연락: 2024-06-01
이름: 김영수, 나이: 73, 독거, 최근연락: 2024-03-15

[Custom GPT 응답]
분석 결과:

1. 이순자 (78세)
   우선순위: 8/10
   ⚠️ 재확인 필요
   이유: 고령 독거, 정기 확인 권장
   
2. 김영수 (73세)
   우선순위: 9/10
   ⚠️⚠️ 긴급 재확인 필요
   이유: 연락 두절 3개월
   → 사망/입원 가능성, 주민등록 확인 필수
```

만족스러우면 "Save" 클릭!

#### Step 4: 공유 및 배포

**공유 설정:**
- **Only me**: 나만 사용
- **Anyone with the link**: 링크 아는 사람 모두 사용
- **Public**: 전체 공개 (GPT Store에 등록)

**구산구청 케이스:**
- "Anyone with the link" 선택
- 링크를 전 직원에게 공유
- 누구나 일관된 품질로 검증 가능

### 4. 실전 응용

#### 응용 1: 민원 응대 봇

**목적:** 주차/건축/세금 민원에 맞춤 답변

```
[Instructions]
You are a civil affairs assistant.
Respond to citizen inquiries about parking, building permits, and taxes.

Always:
- Be polite and formal (Korean 존댓말)
- Provide step-by-step guidance
- Include contact info for follow-up

[Knowledge Files]
- 주차 위반 처리 매뉴얼.pdf
- 건축 허가 가이드.pdf
```

#### 응용 2: 계약서 검토 봇

**목적:** 계약서 위험 조항 자동 탐지

```
[Instructions]
You are a contract review assistant.
Analyze contracts and flag risky clauses.

Flag:
- Penalty clauses over 10%
- Auto-renewal without notice
- Unclear termination conditions

[Knowledge Files]
- 표준 계약서 양식.docx
- 계약 체크리스트.pdf
```

#### 응용 3: 예산 분석 봇

**목적:** 부서별 예산 집행률 분석

```
[Instructions]
You are a budget analysis assistant.
Analyze department budgets and suggest reallocation.

Always:
- Calculate execution rate (%)
- Identify under-executing departments
- Suggest reallocation options

[Knowledge Files]
- 2024년 예산 편성 지침.pdf
```

### 5. Custom GPT vs 일반 ChatGPT

| 기능 | 일반 ChatGPT | Custom GPT |
|------|--------------|------------|
| 프롬프트 | 매번 입력 | 미리 설정 |
| 전문성 | 범용 | 특화 |
| 지식 파일 | 매번 업로드 | 한 번만 업로드 |
| 공유 | 불가능 | 링크로 공유 |
| 일관성 | 사람마다 다름 | 누구나 동일 |

### 6. 고급 기능

#### Actions (API 연동)

Custom GPT에 **외부 시스템**을 연결할 수 있습니다.

**예시: 주민등록 DB 연동**

```
[Action]
API: https://gusan-gu.go.kr/api/resident
Method: POST
Input: 이름, 생년월일
Output: 생존 여부, 주소

[Instructions]
When user asks to verify a person,
call the resident API and report the result.
```

이렇게 하면 Custom GPT가 **실시간으로 DB 조회** 가능!

#### DALL-E, Code Interpreter 활성화

```
[Capabilities]
✅ Web Browsing (실시간 검색)
✅ DALL-E Image Generation (이미지 생성)
✅ Code Interpreter (데이터 분석, 그래프)
```

선택하면 Custom GPT가 **더 많은 기능** 사용 가능.

### 7. 주의사항

**❌ Custom GPT의 한계:**
1. **ChatGPT Plus 필수** (무료 버전 X)
2. **완벽하지 않음** (여전히 오류 가능)
3. **민감 정보 주의** (업로드한 파일은 서버 저장)

**✅ 해야 할 것:**
1. **테스트 충분히** (실전 배포 전)
2. **사람이 최종 확인** (AI는 보조)
3. **정기 업데이트** (매뉴얼 변경 시 재업로드)

### 8. 구산구청 케이스 요약

**윤서연의 작업:**
1. **목적 정의**: 복지 대상자 검증
2. **플래그 기준**: 연락 두절 3개월, 고령 독거
3. **투명성 강조**: 판단 근거 반드시 설명
4. **지식 없음**: (나중에 매뉴얼 추가 가능)
5. **공유**: 전 직원에게 링크 배포

**결과:**
- 김영수 씨 같은 케이스 자동 필터링
- 전 직원 일관된 품질 유지
- 기자회견에서 투명성 입증

---

## 💬 Outro

민준은 창밖을 바라봤습니다.

구산구의 낡은 건물들. 하지만 그 안에서 혁신이 일어나고 있었습니다.

박소희가 말했습니다.

"민준 씨, 다음 주에 전국 지자체 경진대회래요. 나갈래요?"

민준은 웃었습니다.

"네, 과장님. 가죠."

**Phase 3 완료. 다음 화에서 계속...**

---

**[Ep 8 초안 완료]**
- 소설 분량: 4,380자 (공백 포함)
- 튜토리얼 분량: 1,680자
- Visual Placeholder: 5개