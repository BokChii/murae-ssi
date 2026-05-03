# 무래씨 컵물회 — 자산 확보 체크리스트

> 랜딩 페이지 v0.2 기준 / 모든 파일은 `images/` 폴더에 저장
> 우선순위: 🔴 Critical → 🟡 Important → 🟢 Nice-to-have

---

## 📦 이미 보유한 자산 (정리만 필요)

| 자산 | 현재 상태 | 액션 |
|---|---|---|
| 영일대 정자 사진 | 채팅에 업로드 | `images/01-yeongildae-ocean.jpg`로 저장 |
| 완성 컵물회 사진 (흰배경) | 채팅에 업로드 | `images/02-cup-finished.jpg`로 저장 |
| 시장 컵 든 손 사진 | 채팅에 업로드 | `images/03-lifestyle-market.jpg`로 저장 |
| 무래씨 캐릭터 디자인 | 디자인 파일 보유 | PNG 추출 후 다양한 포즈로 변형 (아래 참조) |
| 컵 인쇄 디자인 (스카이라인 버전) | 디자인 파일 보유 | PNG 추출 |
| 컵 홀더 디자인 | 디자인 파일 보유 | PNG 추출 |

---

## 🔴 Critical — 페이지 완성도의 절반

### A. 무래씨 캐릭터 PNG 시리즈 (5장)

기존 캐릭터 디자인에서 포즈 변형해서 PNG로 추출. 디자이너에게 한 번에 의뢰하면 효율적.

| 파일명 | 포즈 | 사용처 | 사이즈 |
|---|---|---|---|
| `images/murae-front.png` | 정면, 컵 들고 있음 | Hero 작은 마크 | 512×512 PNG (투명 배경) |
| `images/murae-wave.png` | 손 흔드는 인사 | Cup Story reveal, CTA | 512×640 PNG (투명 배경) |
| `images/murae-side.png` | 측면, 컵 가리키는 | (선택, 추후 활용) | 512×640 PNG |
| `images/murae-mini.png` | 작은 마스코트 (Hero 상단 로고) | Top nav 영역 | 128×128 PNG |
| `images/murae-laughing.png` | 웃는 표정 클로즈업 | (선택, SNS·OG용) | 512×512 PNG |

**확보 방법**: 기존 무래씨 디자이너에게 "5포즈 추가 작업" 한 번에 의뢰. 단가 협상 필요. 또는 기존 디자인 파일을 본인이 직접 변형 (Procreate, Illustrator).

---

### B. 컵 시퀀스 사진 (Cup Story 핵심)

**Option 1 (최소): SVG 컵 유지** — 현재 프로토타입처럼 SVG 컵 + 색상 레이어로 처리. 추가 사진 불필요.

**Option 2 (권장): 실사 5장 시퀀스** — 모던/영한 톤 강화에 가장 큰 임팩트.

| 파일명 | 단계 | 촬영 가이드 | 사이즈 |
|---|---|---|---|
| `images/cup-stage-1-empty.png` | 빈 컵 | 흰 배경, 위에서 약간 내려본 각도 | 1200×1600 PNG |
| `images/cup-stage-2-veggies.png` | 채소 추가 | 동일 각도/조명 | 1200×1600 PNG |
| `images/cup-stage-3-sauce.png` | 양념 추가 | 동일 각도/조명 | 1200×1600 PNG |
| `images/cup-stage-4-fish.png` | 회·고명 추가 | 동일 각도/조명 | 1200×1600 PNG |
| `images/cup-stage-5-finished.png` | 완성 (IMG-02 활용 가능) | — | — |

**촬영 가이드**:
- 설머리에서 시제품 만드시는 동안 5단계를 순차로 촬영
- 같은 위치, 같은 각도(살짝 내려본 30도 정도), 같은 조명
- 배경은 흰 천 또는 백호리존
- 핸드폰 충분, 다만 삼각대 또는 고정대 필수
- RAW로 찍을 수 있으면 RAW (후보정 여지)
- 30분이면 끝남

**대안**: 실사가 어려우면 → AI 일러스트 5장 시리즈 (Midjourney, "korean cup mulhoe step by step illustration, 5 stages, isolated white background")

---

### C. Cup Story 측면 재료 cutout (4장)

컵 옆에서 슬라이드인 되는 재료 cutout. 흰 배경에서 PNG cutout으로.

| 파일명 | 내용 | 사용처 |
|---|---|---|
| `images/ing-pear.png` | 배 슬라이스 (몇 조각) | Stage 2 좌측 |
| `images/ing-cucumber.png` | 오이 채 (몇 갈래) | Stage 2 우측 |
| `images/ing-fish.png` | 회 슬라이스 (광어/우럭) | Stage 4 좌측 |
| `images/ing-garnish.png` | 깨 + 김 + 견과 | Stage 4 우측 |

**촬영 가이드**: 위 컵 시퀀스 촬영 때 같이 한 컷씩. 흰 천 위에 단독으로 놓고 위에서 촬영. 후보정으로 배경 제거하여 PNG.

**대안**: AI 생성 (배경 transparent로 출력 가능한 Flux, Adobe Firefly 등)

---

### D. 라이프스타일 사진 2장

| 파일명 | 장면 | 가이드 |
|---|---|---|
| `images/lifestyle-car.jpg` | 차 안에서 컵 들고 있는 손 | 운전석 옆 컵홀더 또는 무릎 위 컵, 차창 너머 흐리게 영일대 |
| `images/lifestyle-friends.jpg` | 친구와 마주 앉아 컵 사이 | 영일대 벤치/카페 야외, 두 손이 컵을 마주 잡거나 컵 두 개가 마주 보고 있는 구도 |

**촬영 가이드**:
- 사람 얼굴은 흐릿하게 또는 안 나오게(개인정보, 모델 동의 이슈)
- 컵 + 손 + 배경(바다/거리) 구도가 핵심
- 골든아워(일몰 직전 1시간) 촬영 강력 권장 — 같은 사진도 톤이 완전히 달라짐
- 친구 1~2명 동원해서 30분 안에 가능

**대안**: 팝업 행사 진행하면서 자연스러운 컷 확보 후 v0.3에서 교체 — 그때까지는 현재 placeholder 유지

---

## 🟡 Important — 디테일 완성도

### E. 굿즈 mockup (4장)

| 파일명 | 내용 | 확보 |
|---|---|---|
| `images/goods-cup-print.png` | 컵 펼쳐진 인쇄 디자인 | 기존 디자인 파일에서 PNG 추출 |
| `images/goods-holder.png` | 컵 홀더 펼쳐진 모습 | 기존 디자인 파일에서 PNG 추출 |
| `images/goods-keychain.png` | 무래씨 키링 mockup | Figma/Photoshop에서 아크릴 키링 mockup 합성 |
| `images/goods-sticker.png` | 무래씨 스티커 시트 | 디자인 후 mockup |

**키링·스티커 mockup 빠르게 만드는 법**:
- 무료: [Smartmockups](https://smartmockups.com/), [Mockey](https://mockey.ai/)
- 무래씨 캐릭터 PNG 업로드 → 키링/스티커 mockup 자동 합성
- 5분이면 끝

---

### F. 설머리 매장 사진 (선택, 1~2장)

| 파일명 | 내용 |
|---|---|
| `images/seolmeori-exterior.jpg` | 설머리 매장 외관 |
| `images/seolmeori-interior.jpg` | (선택) 사장님 작업 모습 또는 인테리어 |

**가이드**: 사장님 양해 받고 핸드폰으로. 외관 정면 1장이면 충분. 인테리어는 인물 노출 주의.

---

### G. 메타·SEO 자산

| 파일명 | 사이즈 | 용도 |
|---|---|---|
| `images/og-image.jpg` | 1200×630 | 인스타·카톡·트위터 공유 미리보기 |
| `images/favicon.ico` | 32×32 (멀티 사이즈) | 브라우저 탭 아이콘 |
| `images/apple-touch-icon.png` | 180×180 | iOS 홈화면 |
| `images/instagram-profile.png` | 320×320 | @murae.ssi 인스타 프로필 |

**OG 이미지 디자인 가이드**: 무래씨 + "포항 컵물회 · 9,000원" + 무래씨 캐릭터를 큰 비주얼로. Figma/Canva 30분 작업.

---

## 🟢 Nice-to-have — 모던/영한 톤 강화 (현재 부족하다고 느끼는 부분)

### H. 비디오 자산 (가장 큰 임팩트)

영상이 들어가면 페이지가 즉시 살아납니다. 정적 사진 → 모션으로 가는 것이 "모던/영한" 느낌의 결정적 차이.

| 파일명 | 길이 | 내용 | 사용처 |
|---|---|---|---|
| `videos/hero-ocean.mp4` | 8~12s 루프 | 영일대 잔파도 close-up, 또는 저녁놀 변화 | Hero 풀블리드 (현재 정사진 대체) |
| `videos/cup-pour.mp4` | 5~8s | 양념이 컵에 부어지는 슬로모션 | (선택) Cup Story 양념 단계 |
| `videos/walking.mp4` | 6~10s 루프 | 영일대 산책로 1인칭 워킹뷰 + 컵 들고 있는 손 | Lifestyle 카드 hover 시 재생 |

**촬영 가이드**:
- 핸드폰 4K 60fps로 촬영 → 1080p 30fps로 압축 (HandBrake 무료)
- 1MB 이하로 압축 (모바일 데이터 고려)
- 무음 (autoplay 제약 회피)
- mp4 + H.264 코덱
- 스마트폰 짐벌 있으면 좋지만 없어도 됨

**임팩트**: Hero 영상 하나만 추가해도 페이지 인상이 두 배 이상 달라짐. 영일대 가실 때 10초 영상 한 컷만 찍어와도 충분.

---

### I. Lottie 애니메이션 (선택, 고급)

무래씨가 살아 움직이는 느낌을 위해.

| 파일 | 내용 | 확보 |
|---|---|---|
| `animations/murae-wave.json` | 무래씨가 손 흔드는 루프 | LottieFiles 무료 일부 활용 또는 일러스트레이터 + AfterEffects |
| `animations/cup-pouring.json` | 양념 부어지는 모션 | 동상 |

**대안**: APNG (애니메이션 PNG)로 GIF 대체. 일러스트레이터에서 프레임 작업 후 APNG 변환.

---

### J. 추가 사진 (스토리텔링 강화)

| 파일명 | 내용 |
|---|---|
| `images/story-process-1.jpg` | 사장님이 회 다듬는 손 클로즈업 |
| `images/story-process-2.jpg` | 컵에 양념 따르는 모먼트 |
| `images/story-pohang-1.jpg` | 영일대 일몰 |
| `images/story-pohang-2.jpg` | 죽도시장 사람들 (멀리서, 뒷모습) |

**용도**: 추후 "About" 또는 "Story" 섹션 추가 시 활용

---

## 🛠️ 자산 확보 매트릭스 (한눈에)

| 카테고리 | 양 | 확보 방법 | 예상 시간 | 예상 비용 |
|---|---|---|---|---|
| 무래씨 포즈 PNG | 5장 | 디자이너 의뢰 | 1~2주 | 5~15만원 |
| 컵 시퀀스 사진 | 5장 | 설머리 1세션 촬영 | 1시간 | 0원 |
| 측면 재료 cutout | 4장 | 동상 + 후보정 | +30분 | 0원 |
| 라이프스타일 사진 | 2장 | 친구 동원, 영일대 | 1시간 | 0원 |
| 굿즈 mockup | 4장 | Smartmockups + Figma | 2시간 | 0원 (무료 도구) |
| 매장 사진 | 1~2장 | 핸드폰 | 5분 | 0원 |
| OG·favicon | 4장 | Figma/Canva | 1시간 | 0원 |
| 비디오 (Hero) | 1편 | 영일대 핸드폰 촬영 | 30분 | 0원 |
| Lottie 애니메이션 | 1~2편 | 디자이너 의뢰 또는 LottieFiles | 1~2주 | 5~10만원 또는 0원 |

**최소 출발 패키지** (무료, 1주 안에 완성):
- 무래씨 PNG 추출 (직접)
- 컵 시퀀스 5장 (설머리 1세션)
- 측면 재료 4장 (동상)
- 라이프스타일 2장 (친구 동원)
- 굿즈 mockup 4장 (Smartmockups)
- OG·favicon (Canva)
- Hero 비디오 (영일대 핸드폰)

→ 이걸로 페이지 90% 완성. 무래씨 5포즈 디자이너 의뢰는 병행 진행.

---

## 📋 촬영 일정 제안

**Day 1 — 설머리 (90분)**
- 컵 시퀀스 5장
- 측면 재료 cutout 4장
- (선택) 사장님 작업 영상 30초

**Day 2 — 영일대 (90분, 일몰 시간 맞춰)**
- Hero용 바다 영상 1편 (10초)
- 라이프스타일 사진 2장 (친구 동반)
- (선택) 일몰·산책로 풍경 추가

**Day 3 — 데스크 작업 (3시간)**
- 무래씨 PNG 추출/정리
- 굿즈 mockup 합성
- OG·favicon 디자인
- 사진 후보정 (Lightroom/Snapseed)

**Day 4 — 디자이너 회신 대기 + 페이지 교체**
- 무래씨 5포즈 받으면 → 페이지 자산 교체
- v0.3 점검

---

## 💡 모던/영한 톤 강화를 위한 추가 제안

현재 v0.2가 약간 부족하다고 느끼시는 모던/영한 톤은 — **자산 추가**로 거의 다 해결됩니다. 코드를 갈아엎는 게 아니라.

1. **Hero에 영상 1편** → 즉시 8할 해결
2. **컵 시퀀스 실사 5장** → Cup Story가 진짜 음식 광고 톤으로 격상
3. **라이프스타일 골든아워 사진** → 페이지 전체 색감이 따뜻하고 vivid해짐
4. **무래씨 다양한 포즈** → 페이지에 "캐릭터가 살아 있다"는 느낌

이 4가지가 들어오면 v0.3에서 재확인 시 톤이 확 달라져 있을 거예요.

---

## 🎯 다음 단계

1. 이 체크리스트 보고 어떤 것부터 확보할지 우선순위 정하기
2. 설머리 사장님께 촬영 일정 잡기 (최우선)
3. 무래씨 디자이너에게 5포즈 의뢰 (병행)
4. 자산 들어오는 대로 `images/` 폴더에 저장 → 새로고침 → 페이지가 점점 살아남
5. 모든 자산 들어오면 v0.3 점검 + 미세 디자인 조정

자산 확보하면서 막히는 부분 있으면 (촬영 가이드, AI 프롬프트, mockup 도구 등) 바로 알려주세요.
