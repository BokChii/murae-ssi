# 무래씨 — AI 자산 생성 프롬프트 가이드

> 모든 프롬프트는 영문 (대부분의 AI 모델이 영문에서 결과 품질이 더 안정적)
> 결과물은 `images/` 또는 `videos/` 폴더에 명시된 파일명으로 저장

---

## 🛠️ 도구 추천 매트릭스

| 카테고리 | 1순위 | 2순위 | 비고 |
|---|---|---|---|
| **컵 시퀀스 (일관성 필수)** | ChatGPT 4o (DALL·E) | Midjourney v6 (--seed 고정) | 4o가 "동일한 컵 유지" 능력이 압도적 |
| **재료 cutout (투명 배경)** | Adobe Firefly | Flux Pro + 배경 제거 | Firefly가 PNG transparent 직출력 |
| **라이프스타일 사진** | Midjourney v6 | Flux 1.1 Pro | 시네마틱 톤은 Midjourney 우세 |
| **잔파도 영상** | Veo 3 (Google) | Kling 2.0 / Runway Gen-4 | Veo가 자연 풍경 압도적 |
| **양념 부어지는 슬로모션** | Kling 2.0 | Runway Gen-4 / Sora | Kling이 액체 모션 강함 |

---

## 🎨 공통 스타일 가이드 (모든 프롬프트에 공통)

**Cup 시리즈 공통 톤**:
- Modern food photography
- Bright cinematic lighting
- Clean white seamless background
- Slight overhead 30° angle (consistent across all 5 stages)
- Magazine quality
- Sharp focus, vibrant fresh colors
- 16oz clear plastic takeout cup (PET)

**Lifestyle 시리즈 공통 톤**:
- Golden hour lighting (일몰 직전 1시간)
- Magazine editorial quality
- Modern young aesthetic
- Pohang, Korea (Yeongildae) setting
- Warm soft tones
- Faces out of frame or from behind (개인정보·AI 약점 회피)

---

## 📸 PART 1 — 컵 시퀀스 5장 (가장 중요, 일관성 핵심)

### 🔑 일관성 확보 전략

**Best practice (강력 추천)**: ChatGPT 4o 한 채팅창에서 순차로 생성
1. 빈 컵 1장 먼저 생성 → 마음에 들면 픽스
2. 같은 채팅에서 "이 컵에 채소를 채워줘" 식으로 edit 요청
3. 4o는 이전 이미지의 컵 형태/각도/조명을 기억함

**대안**: Midjourney v6 + `--seed [숫자]` + `--cref [이미지URL]` 사용

저장명: `cup-stage-1-empty.png` ~ `cup-stage-5-finished.png`
권장 사이즈: 1024×1280 (4:5)

---

### 1️⃣ Stage 1 — 빈 컵 (`cup-stage-1-empty.png`)

```
A clear plastic 16oz takeout cup, empty, no lid, isolated on pure white seamless studio background, slight overhead 30-degree angle, professional food photography, sharp focus, soft studio lighting, subtle natural shadow under cup, vibrant clean modern aesthetic, no text or logo on cup, condensation-free, magazine quality

--ar 4:5 --style raw --v 6
```

**Negative prompt** (Midjourney/SD 사용 시):
```
text, logo, watermark, brand name, table, hand, multiple cups
```

---

### 2️⃣ Stage 2 — 채소 추가 (`cup-stage-2-veggies.png`)

ChatGPT 4o에서 Stage 1 이미지 보내고:
```
같은 컵에 신선한 채 썬 야채를 채워줘 — 오이 채, 양배추 채, 배 슬라이스, 당근 채. 컵의 60% 정도까지 채워지게. 다른 모든 요소(컵 모양, 각도, 배경, 조명)는 그대로 유지.
```

또는 직접 프롬프트:
```
A clear plastic 16oz takeout cup filled 60% with shredded fresh vegetables — julienned cucumber, shredded cabbage, thin Korean pear slices, julienned carrot, isolated on pure white seamless studio background, slight overhead 30-degree angle, identical cup shape and angle as previous shot, professional food photography, sharp focus, vibrant fresh colors, magazine quality

--ar 4:5 --style raw --v 6
```

---

### 3️⃣ Stage 3 — 양념 추가 (`cup-stage-3-sauce.png`)

ChatGPT 4o:
```
같은 컵에 빨간 한국 물회 양념(고추장 베이스)을 컵 바닥에서 위로 올라오게 부어진 상태로 만들어줘. 양념이 야채를 절반쯤 덮고 있고 깨가 떠 있게. 다른 요소는 동일.
```

직접 프롬프트:
```
A clear plastic 16oz takeout cup with vibrant red Korean spicy mulhoe sauce (gochujang-based) filling the bottom 50%, with shredded vegetables on top half, sesame seeds floating in sauce, glossy sauce texture with visible droplets, isolated on pure white seamless studio background, slight overhead 30-degree angle, identical cup as before, professional food photography, dramatic vibrant red color, sharp focus, magazine quality

--ar 4:5 --style raw --v 6
```

---

### 4️⃣ Stage 4 — 회·고명 추가 (`cup-stage-4-fish.png`)

ChatGPT 4o:
```
같은 컵에 가자미회 슬라이스를 야채 위에 얹고, 깨와 견과류를 토핑으로 올려줘. 빨간 양념은 아래 절반에 그대로 보이게. 다른 요소 동일.
```

직접 프롬프트:
```
A clear plastic 16oz takeout cup filled with Korean cup mulhoe — layers clearly visible: red spicy sauce at bottom (40%), shredded vegetables in middle (30%), fresh white sole/flounder (gajami) sashimi slices on top (30%), garnished with sesame seeds and crushed peanuts, isolated on pure white seamless studio background, slight overhead 30-degree angle, identical cup as before, professional food photography, sharp focus, vibrant fresh colors, magazine quality

--ar 4:5 --style raw --v 6
```

---

### 5️⃣ Stage 5 — 완성 이미지 (`cup-stage-5-finished.png`)

⚠️ 채팅에 올린 IMG-02(완성 컵물회)와 비슷한 결과물이 필요. 그게 이미 있으니 IMG-02로 대체 가능.

새로 생성하려면:
```
A complete Korean cup mulhoe in a clear plastic 16oz takeout cup with transparent dome lid on top, fully assembled with visible layers — red sauce, vegetables, white fish sashimi, topped with crispy seaweed flakes, sesame seeds and crushed peanuts garnish, condensation droplets on cup exterior suggesting cold freshness, isolated on pure white seamless studio background, slight overhead 30-degree angle, identical cup style as previous stages, professional food photography, dramatic studio lighting, magazine quality, ultra-vibrant colors

--ar 4:5 --style raw --v 6
```

---

## 🥒 PART 2 — 재료 Cutout 4장 (투명 배경 필수)

### 📌 핵심 가이드
- **Adobe Firefly 강력 추천** — "Transparent Background" 옵션으로 PNG 직출력
- 또는 일반 AI 생성 후 [remove.bg](https://www.remove.bg/) 또는 [Photoroom](https://www.photoroom.com/)으로 배경 제거
- 사이즈: 800×800 PNG (정사각, 투명)

---

### 6️⃣ 배 슬라이스 (`ing-pear.png`)

```
Fresh Korean pear (Asian pear / nashi) thin julienne slices, scattered loosely as if just sliced, top-down view, isolated subject with pure white background that can be removed, professional food photography, sharp focus, vibrant fresh pale yellow color, crisp texture visible, magazine quality

--ar 1:1 --style raw --v 6
```

**Adobe Firefly 사용 시**: "Generate" 모드에서 위 프롬프트 + "Background: Transparent" 옵션 체크.

---

### 7️⃣ 오이 채 (`ing-cucumber.png`)

```
Fresh cucumber julienne thin matchstick strips, scattered loosely in a casual cluster, top-down view, isolated subject on pure white removable background, professional food photography, sharp focus, vibrant green color with white interior visible, crisp fresh appearance, dewy texture, magazine quality

--ar 1:1 --style raw --v 6
```

---

### 8️⃣ 가자미회 슬라이스 (`ing-fish.png`)

```
Fresh Korean gajami (sole / right-eye flounder) sashimi slices, sliced thin into rectangular fillet pieces, arranged loosely on pure white removable background, top-down view, isolated subject, professional sushi-grade food photography, glossy translucent fresh fish texture, subtle pink-white tones, sharp focus, premium quality

--ar 1:1 --style raw --v 6
```

---

### 9️⃣ 깨 + 김 + 견과 (`ing-garnish.png`)

```
A scattered mix of toasted white sesame seeds, small crispy roasted seaweed (gim) flakes, and crushed peanuts, dynamic scattered composition on pure white removable background, top-down close-up view, isolated subjects, professional food photography, sharp focus, vivid contrasting colors (white sesame, dark green-black seaweed, golden brown peanuts), --ar 1:1 --style raw --v 6
```

---

## 🌅 PART 3 — 라이프스타일 사진 2장

### 🔟 차 안에서 컵 들고 있는 손 (`lifestyle-car.jpg`)

```
Close-up shot inside a car, focused on a young person's hand gently holding a clear plastic takeout cup of Korean cup mulhoe (red spicy seafood soup with vegetables visible through clear cup), the cup placed on the passenger seat or center console, view through windshield showing blurred ocean and Korean traditional pavilion (jeongja) of Pohang Yeongildae beach in the background, golden hour warm sunlight streaming through windows, bokeh, magazine editorial lifestyle photography, vertical composition, hand only no face visible, modern young Korean aesthetic, soft warm tones, shallow depth of field

--ar 4:5 --style raw --v 6
```

---

### 1️⃣1️⃣ 친구와 마주 앉아 컵 사이 (`lifestyle-friends.jpg`)

```
Lifestyle scene showing two clear plastic takeout cups of Korean cup mulhoe placed close together on a rustic wooden outdoor table, two young people's hands gently holding each cup from opposite sides, faces out of frame, blurred ocean and sandy beach of Pohang Yeongildae in the background with soft bokeh, golden hour warm sunset lighting, magazine editorial photography, vertical composition, intimate friendship moment, modern young Korean aesthetic, warm cinematic tones

--ar 4:5 --style raw --v 6
```

---

## 🎬 PART 4 — 영상 자산 2편

### 📌 영상 도구 가이드

| 도구 | 가격 | 길이 | 품질 | 추천도 |
|---|---|---|---|---|
| **Veo 3** (Gemini) | Pro 멤버십 | 8s | ⭐⭐⭐⭐⭐ | 자연 풍경 압도적 |
| **Kling 2.0** | 무료 일일 + 유료 | 5~10s | ⭐⭐⭐⭐⭐ | 액체·모션 강함 |
| **Runway Gen-4** | $12/월~ | 5~10s | ⭐⭐⭐⭐ | 안정적 |
| **Sora** | ChatGPT Pro | 10~20s | ⭐⭐⭐⭐⭐ | 비싸지만 최고 |

---

### 1️⃣2️⃣ 영일대 잔파도 close-up (`videos/hero-ocean.mp4`)

**Veo 3 / Kling 2.0 프롬프트**:
```
Close-up cinematic shot of small ocean waves gently rolling onto a sandy beach in Korea's East Sea, slow elegant motion, golden hour warm sunlight reflecting on water surface, sparkling highlights, traditional Korean pavilion (jeongja) softly visible in distance on a pier, calm peaceful atmosphere, no people visible, 4K cinematic, seamless loop friendly, soft warm color grading, slight slow motion feel
```

**팁**:
- 8~10초 길이로 생성
- 시작과 끝이 비슷한 프레임이어야 루프가 자연스러움 → "seamless loop" 명시
- 다운로드 후 HandBrake로 1080p, ~1MB 이하로 압축
- 무음으로 export (autoplay 정책)

**압축 설정 (HandBrake)**:
- Format: MP4
- Resolution: 1920×1080
- Framerate: 30fps
- Quality: RF 26-28
- Audio: None

---

### 1️⃣3️⃣ 양념이 컵에 부어지는 슬로모션 (`videos/sauce-pour.mp4`)

**Kling 2.0 / Runway Gen-4 프롬프트**:
```
Ultra slow motion close-up shot of vibrant red Korean spicy gochujang mulhoe sauce being poured from a small ladle into a clear plastic takeout cup containing shredded vegetables and white fish sashimi, dramatic splash and droplets in air, glossy thick sauce texture, white seamless studio background, professional food cinematography, 4K ultra slow motion, vivid saturated red color, soft studio lighting, magazine commercial quality, 5 seconds duration
```

**팁**:
- 5~6초 길이가 적절
- "ultra slow motion" 명시 (자연스러운 슬로모션 효과)
- 첫 프레임은 빈 컵 → 마지막 프레임은 양념 차오른 상태로 자연 종료

---

## 💡 PART 5 — 일관성 유지 핵심 팁

### 컵 시퀀스 5장 일관성 확보 절차

**Method A — ChatGPT 4o (가장 쉬움)**:
1. ChatGPT Plus 또는 Pro 가입
2. 새 채팅 시작
3. Stage 1 프롬프트 입력 → 마음에 드는 빈 컵 생성
4. **같은 채팅창에서** "이 컵에 야채를 채워줘"로 Stage 2
5. 같은 방식으로 Stage 3, 4, 5 진행
6. 각 결과 다운로드

**Method B — Midjourney v6**:
1. Stage 1 빈 컵 생성, 결과 이미지 URL 복사
2. Stage 2~5 프롬프트 끝에 `--cref [Stage1 URL] --cw 80` 추가
3. `--seed` 동일 숫자 사용 (예: `--seed 42`)
4. `--cw 80`은 Character Reference Weight (스타일 일관성 강도)

**Method C — Flux Kontext**:
1. Stage 1 생성
2. Flux Kontext의 image-to-image 모드에서 Stage 1을 base로 사용
3. "Add vegetables to this cup" 식으로 변형

---

### 라이프스타일 2장 일관성

같은 톤 (golden hour + warm tones + Yeongildae) 키워드 반복.
같은 시드 사용하면 컬러그레이딩 통일됨.

---

## 📋 PART 6 — 생성 체크리스트

각 자산 생성 후 체크하세요:

- [ ] Stage 1 빈 컵 → `cup-stage-1-empty.png`
- [ ] Stage 2 채소 → `cup-stage-2-veggies.png`
- [ ] Stage 3 양념 → `cup-stage-3-sauce.png`
- [ ] Stage 4 회·고명 → `cup-stage-4-fish.png`
- [ ] Stage 5 완성 → `cup-stage-5-finished.png` (또는 IMG-02 활용)
- [ ] 배 슬라이스 → `ing-pear.png` (투명 배경)
- [ ] 오이 채 → `ing-cucumber.png` (투명 배경)
- [ ] 가자미회 → `ing-fish.png` (투명 배경)
- [ ] 깨+김+견과 → `ing-garnish.png` (투명 배경)
- [ ] 차 안에서 → `lifestyle-car.jpg`
- [ ] 친구와 마주 → `lifestyle-friends.jpg`
- [ ] 영일대 파도 → `videos/hero-ocean.mp4`
- [ ] 양념 슬로모션 → `videos/sauce-pour.mp4`

---

## ⚙️ PART 7 — 자주 발생하는 이슈 + 대처

| 이슈 | 원인 | 대처 |
|---|---|---|
| 컵 모양이 매번 달라짐 | 모델이 컨텍스트 못 잡음 | ChatGPT 4o 같은 채팅창 사용 / Midjourney --cref |
| 컵에 한글 글자가 들어감 | 모델 환각 | 프롬프트에 "no text, no logo, no characters" 추가 |
| 음식이 너무 인공적/플라스틱 같음 | 일반 모델의 한계 | "Photographic, real food, magazine quality, hyperrealistic" 강조 |
| 한국 음식인데 일본/중국 톤 나옴 | 학습 편향 | "Korean cup mulhoe (Korean spicy raw fish soup)" 명시, "gochujang-based" 추가 |
| 영상이 부자연스럽게 빠름 | 기본값 | "slow motion, 60fps captured" 명시 |
| 영상 화질 떨어짐 | 압축 손실 | 4K로 생성 후 1080p로 내려서 압축 |

---

## 🎯 PART 8 — 추천 작업 순서

1. **Day 1 (1~2시간)**: 컵 시퀀스 5장 — ChatGPT 4o로 한 번에. 가장 시간 듦.
2. **Day 2 (1시간)**: 재료 cutout 4장 — Adobe Firefly로 빠르게.
3. **Day 3 (1시간)**: 라이프스타일 2장 — Midjourney로 시안 여러 개 뽑고 베스트 픽.
4. **Day 4 (~2시간)**: 영상 2편 — Kling/Veo로 시도, 압축, 저장.

총 5~6시간이면 완료. 결과 폴더에 떨궈 넣고 새로고침 → v0.3 페이지가 살아남.

---

## 📎 부록: 무료/저렴 도구 진입 경로

- **ChatGPT 4o**: ChatGPT Plus $20/월, 이미지 생성 포함
- **Adobe Firefly**: Adobe Creative Cloud 가입자 무료 일부 / 단독 $4.99/월
- **Midjourney**: Basic $10/월
- **Kling 2.0**: 일일 무료 크레딧 + 유료 약 $7/월
- **Veo 3**: Google AI Pro $19.99/월 (Gemini Advanced 포함)
- **Runway**: 무료 트라이얼 + Standard $12/월
- **remove.bg**: 무료 50장/월 (한 번에 다 처리)

학생 할인 가능한 도구들 있으니 가입 시 확인.

---

## 🚀 다음 단계

1. 위 프롬프트 그대로 복사 → AI 도구에 붙여넣기
2. 생성된 자산을 `images/` (또는 `videos/`)에 명시된 파일명으로 저장
3. 페이지 새로고침 → 자산이 들어간 v0.3 확인
4. 부족한 부분 디자인 미세조정 (모던 톤 강화 등) → v0.4

자산 생성하면서 결과가 마음에 안 들거나 프롬프트 미세조정 필요하면 그때그때 알려주세요.
