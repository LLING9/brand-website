# Pethroom Design Guide

> Design System Analysis — pethroom.com 분석 기반  
> Generated: 2026-04-15 | Updated: 2026-04-15 (v3 — 한글 우선 원칙 반영)  
> Tags: E-Commerce · Pet Brand · Minimalist · Korean Market · VIP Membership

pethroom.com 분석을 바탕으로 도출한 컬러·타이포·레이아웃·컴포넌트 패턴 정리서입니다. 반려동물 브랜드 사이트 제작 시 레퍼런스로 활용하세요.

---

## 타겟 고객 & 언어 원칙 (v3 추가)

### 타겟 고객 정의

| 항목 | 내용 |
|------|------|
| 국적 | 한국인 |
| 연령 | 20–30대 |
| 특성 | 반려동물 보호자 (강아지·고양이 양육 중) |
| 디지털 친숙도 | 높음 — 모바일 쇼핑, SNS 활용 적극적 |
| 구매 동기 | 반려동물 건강·행복 최우선, 품질 신뢰 중시 |
| 언어 환경 | 한국어가 모국어, 영어 병기는 브랜드 인식에만 허용 |

### 언어 사용 대원칙

> **사용자가 행동을 취해야 하는 모든 UI 요소는 한글을 사용한다.**

| 구분 | 원칙 | 예시 |
|------|------|------|
| **내비게이션 메뉴** | 반드시 한글 | Shop ❌ → 쇼핑 ✅ |
| **행동 유도 버튼 (CTA)** | 반드시 한글 | Buy Now ❌ → 구매하기 ✅ |
| **카테고리 탭** | 반드시 한글 | FOR DOG ❌ → 강아지 ✅ |
| **폼 요소** (placeholder, label) | 반드시 한글 | Email ❌ → 이메일 ✅ |
| **브랜드명 / 로고** | 영문 허용 | pawly, VIP ✅ |
| **상품 배지** | 한글 권장 | BEST → 베스트, NEW → 신상품 |
| **섹션 소제목 레이블** | 한글 권장 | BEST SELLERS → 베스트셀러 |
| **수상·인증 명칭** | 영문 유지 | Red Dot Award ✅ (고유 명칭) |

### 이 원칙이 필요한 이유

- 20–30대 한국 사용자는 영문 UI에 익숙하지 않을 경우 **행동 결정 지연** 또는 **이탈**이 발생
- "Shop", "FOR DOG", "EVENT" 같은 단어는 의미는 알지만 **즉각적 반응(reflexive action)** 을 방해함
- 국내 주요 이커머스 (쿠팡, 오늘의집, 무신사)는 모두 내비게이션과 버튼을 **100% 한글** 처리
- 브랜드 아이덴티티 유지가 필요한 **로고·브랜드명·수상명**만 예외로 영문 허용

---

## 목차

1. [Color System](#01-color-system)
2. [Typography](#02-typography)
3. [Spacing Scale](#03-spacing-scale)
4. [Grid & Layout](#04-grid--layout)
5. [Header Component](#05-header-component)
6. [Buttons](#06-buttons)
7. [Badges & Labels](#07-badges--labels)
8. [Product Cards](#08-product-cards)
9. [Section Patterns](#09-section-patterns)
10. [Effects & Motion](#10-effects--motion)
11. [Navigation Structure](#11-navigation-structure)
12. [Do's & Don'ts](#12-dos--donts)

---

## 01 Color System

페스룸은 무채색(블랙·화이트·그레이) 기반의 미니멀리스트 팔레트 위에 오렌지를 핵심 액센트로 사용합니다. 화려하지 않고 제품이 돋보이도록 배경은 항상 중립적으로 유지합니다.

### Primary Palette

| 이름 | Hex | 용도 |
|------|-----|------|
| Orange | `#FF5A1F` | CTA 버튼, 할인 배지, 액센트 |
| Orange Light | `#FF7A42` | 호버 상태, 그라디언트 |
| Orange Pale | `#FFF0EB` | 배경 틴트, 호버 피드백 |
| Black | `#1A1A1A` | 주요 텍스트, 기본 버튼 |
| White | `#FFFFFF` | 배경, 카드 표면 |

### Neutral Scale

| 이름 | Hex | 용도 |
|------|-----|------|
| Gray 90 | `#2C2C2C` | 서브 헤딩, 강조 텍스트 |
| Gray 60 | `#767676` | 보조 텍스트, 메타 정보 |
| Gray 40 | `#ABABAB` | 비활성화, 원래 가격 |
| Gray 20 | `#E0E0E0` | 보더, 구분선 |
| Gray 10 | `#F5F5F5` | 배경, 이미지 플레이스홀더 |

### Semantic Colors

| 이름 | Hex | 용도 |
|------|-----|------|
| Red / Sale | `#E8232C` | 할인가, 품절, 경고 |
| VIP Gold | `#C9A84C` | VIP 멤버십, 프리미엄 배지 |
| Promo Dark | `#1A1A1A` | 프로모션 배너 배경 |

> ⚠️ 오렌지(`#FF5A1F`)는 CTA와 강조에만 사용합니다. 텍스트 색상으로 대량 사용하면 가독성이 저하됩니다.

---

## 02 Typography

한국어 중심 사이트이므로 Noto Sans KR 혹은 Pretendard를 기본 폰트로 사용합니다. 명조체는 사용하지 않으며 전반적으로 Sans-serif 계열로 통일해 모던하고 깔끔한 인상을 줍니다.

### Font Stack

| 역할 | Font Family | Fallback | 비고 |
|------|-------------|----------|------|
| Primary (KO) | `Pretendard` | `Noto Sans KR, Apple SD Gothic Neo` | 한글 최적화 Variable 폰트 |
| Primary (EN) | `Pretendard` | `Inter, Helvetica Neue` | 영문도 자연스럽게 처리 |
| Mono / Code | `JetBrains Mono` | `Consolas, monospace` | 가격·수치 강조 시 선택 사용 |

### Type Scale

| 레벨 | 크기 | Weight | Letter Spacing | Line Height | 용도 |
|------|------|--------|----------------|-------------|------|
| Display | 38–40px | 900 | -1.5px | 1.15 | 섹션 히어로 타이틀 |
| Heading 1 | 26–28px | 800 | -0.5px | 1.25 | Best Seller, New Arrival 섹션 타이틀 |
| Heading 2 | 18–20px | 700 | — | 1.35 | 카드 소제목, 상품명 |
| Body | 14–15px | 400–500 | — | 1.65 | 상품 설명, 일반 텍스트 |
| Caption / Label | 11–12px | 600–700 | 0.5–1px | — | 브랜드명, 카테고리 태그 (uppercase) |

### Price Typography

```
₩41,600   → font-size: 18px / weight: 900 / color: #E8232C
₩52,000   → font-size: 13px / weight: 400 / color: #ABABAB / text-decoration: line-through
VIP가      → Gold badge (#C9A84C) + bold amount
```

---

## 03 Spacing Scale

4px 기본 단위(4pt grid)를 사용합니다. 컴포넌트 내부 패딩은 작은 단위, 섹션 간 간격은 큰 단위를 적용해 시각적 리듬을 만듭니다.

| 토큰 | 값 | 용도 |
|------|-----|------|
| `--space-1` | 4px | 마이크로 간격 |
| `--space-2` | 8px | 인라인 요소 간격 |
| `--space-3` | 12px | 소형 패딩 |
| `--space-4` | 16px | 카드 내부 기본 패딩 |
| `--space-6` | 24px | 카드 간격, 그리드 gap |
| `--space-8` | 32px | 서브섹션 마진 |
| `--space-12` | 48px | 섹션 상하 패딩 (모바일) |
| `--space-16` | 64px | 섹션 상하 패딩 (데스크톱) |
| `--space-20` | 80px | 주요 섹션 간격 |

---

## 04 Grid & Layout

컨텐츠 최대 너비는 1200–1280px이며 좌우 24px 패딩으로 페이지 여백을 확보합니다. 제품 그리드는 맥락에 따라 4–6열로 유연하게 변합니다.

### Container & Breakpoints

| 이름 | 너비 | 컬럼 | 용도 |
|------|------|------|------|
| Mobile | `≤ 768px` | 2열 | 상품 2개씩, 스택 레이아웃 |
| Tablet | `769–1024px` | 3열 | 상품 3개씩 |
| Desktop | `1025–1280px` | 4열 | 상품 4개씩 (Best Seller) |
| Wide | `≥ 1281px` | 5–6열 | 카테고리, 인기 상품 섹션 |

### Grid Variants

```
4-col (Desktop / Best Seller)
[ 1 ] [ 2 ] [ 3 ] [ 4 ]

6-col (Wide / Category Grid)
[ 1 ] [ 2 ] [ 3 ] [ 4 ] [ 5 ] [ 6 ]

2-col (Promo Banner)
[ 프로모 A ] [ 프로모 B ]
```

### Page Layout Diagram

```
┌─────────────────────────────────────────────────────┐
│  🔔 상단 공지 배너  (bg: #FF5A1F · h: 36px)          │
├─────────────────────────────────────────────────────┤
│  🖤 프로모션 바  (bg: #1A1A1A · h: 40px)             │
├─────────────────────────────────────────────────────┤
│  🏠 헤더  (bg: white · h: 60–72px · sticky)         │
├─────────────────────────────────────────────────────┤
│  📂 서브 카테고리 바  (bg: #F5F5F5 · h: 40px)        │
├─────────────────────────────────────────────────────┤
│  🎯 히어로 / 메인 배너 슬라이더                       │
├─────────────────────────────────────────────────────┤
│  ⭐ Best Seller  (4-col grid)                        │
├─────────────────────────────────────────────────────┤
│  🆕 New Arrival  (4–6 col grid)                     │
├─────────────────────────────────────────────────────┤
│  🥗 큐레이션 / 테마 특집                              │
├─────────────────────────────────────────────────────┤
│  📱 App 프로모션 배너  (full-width · dark bg)         │
├─────────────────────────────────────────────────────┤
│  💡 IoT 기기 섹션                                    │
├─────────────────────────────────────────────────────┤
│  🌱 CSR / 사회공헌 섹션                               │
├─────────────────────────────────────────────────────┤
│  🦶 Footer  (bg: #0F0F1A · dark)                    │
└─────────────────────────────────────────────────────┘
```

---

## 05 Header Component

헤더는 3-tier 구조로 구성됩니다: 상단 공지 바 → 프로모션 바 → 메인 헤더. sticky 적용 시 메인 헤더만 고정합니다.

### Header Layer Specs

| 레이어 | 배경색 | 텍스트색 | 높이 |
|--------|--------|----------|------|
| 공지 배너 | `#FF5A1F` | `#FFFFFF` | 36px |
| 프로모션 바 | `#1A1A1A` | `rgba(255,255,255,0.7)` | 40px |
| 메인 헤더 | `#FFFFFF` | `#1A1A1A` | 60–72px |
| 서브 카테고리 바 | `#F5F5F5` | `#767676` | 40px |

### Header Structure

```
[ 공지 배너: 신규 회원가입 시 10% 즉시 할인 쿠폰 지급 ]
[ VIP 회원 35% 추가 할인 | 정기배송 신청 시 무료배송 | 오늘의 특가 마감 D-1 ]
[ PETHROOM   SHOP · VIP CENTER · FRIENDS · EVENT · About · Community   🚚 🔍 👤 🛒 ]
[ ALL | NEW | BEST | FOR DOG | FOR CAT | 사료/영양 | 간식 | 위생용품 | COLLABO ]
```

---

## 06 Buttons

버튼은 최소화된 border-radius(4px)를 사용해 테크니컬하고 신뢰감 있는 인상을 줍니다. 원형 버튼은 사용하지 않습니다.

### Button Variants

| 타입 | 배경색 | 텍스트색 | 용도 |
|------|--------|----------|------|
| Primary (Black) | `#1A1A1A` | `#FFFFFF` | 장바구니 담기, 구매하기 |
| CTA (Orange) | `#FF5A1F` | `#FFFFFF` | VIP 혜택 보기, 앱 다운로드 |
| Secondary (Outline) | 투명 | `#1A1A1A` | 상세보기, 전체보기 |
| Ghost (Gray) | 투명 | `#767676` | 취소, 더보기 |
| Small Black | `#1A1A1A` | `#FFFFFF` | 담기 |
| Small Orange | `#FF5A1F` | `#FFFFFF` | 쿠폰받기 |
| Small Outline | 투명 | `#1A1A1A` | 품절알림 |

### Button Specs

| 속성 | 값 |
|------|-----|
| `border-radius` | `4px` (원형 버튼 비사용) |
| `font-weight` | `700` |
| `padding (md)` | `12px 28px` |
| `padding (sm)` | `7px 16px` |
| `hover opacity` | `0.85` 또는 배경색 10% 어둡게 |
| `transition` | `opacity 0.2s ease` |

---

## 07 Badges & Labels

### Product Badges

| 배지 | 배경색 | 텍스트색 | 용도 |
|------|--------|----------|------|
| SALE | `#E8232C` | White | 할인 적용 상품 |
| BEST | `#1A1A1A` | White | 베스트셀러 |
| NEW | `#FF5A1F` | White | 신규 입고 상품 |
| VIP | `#C9A84C` | White | VIP 전용 혜택 |
| 품절 | `#F5F5F5` | Gray 60 | 재고 없음 |
| MD PICK | `#2C7A7B` | White | 에디터 추천 |

### Label Variants

```
VIP 35% 추가할인  → bg: #FFF0EB / color: #FF5A1F / padding: 4px 12px
오늘만 특가       → bg: #FFF5F5 / color: #E8232C
정기배송 전용     → bg: #F0F4FF / color: #3B5EDB
```

### Badge Specs

| 속성 | 값 |
|------|-----|
| `border-radius` | `3–4px` |
| `font-size` | `10–11px` |
| `font-weight` | `800` |
| `text-transform` | `uppercase` |
| `letter-spacing` | `0.3px` |

---

## 08 Product Cards

페스룸의 핵심 컴포넌트입니다. 가격 구조가 3단계(원가 → 할인가 → VIP가)로 이루어져 있어 카드 내 정보 계층이 중요합니다.

### Card Anatomy

```
┌──────────────────────┐
│   [상품 이미지]        │  ← bg: #F5F5F5 / aspect-ratio: 1:1
│   [BEST] 배지 (좌상)  │
├──────────────────────┤
│ BRAND NAME           │  ← 11px / uppercase / orange
│ 상품명 (2줄 클램프)    │  ← 13-14px / weight 600
│                      │
│ ~~₩52,000~~          │  ← 원가: 13px / gray / line-through
│ ₩41,600              │  ← 할인가: 18px / weight 900 / red
│ [VIP가] ₩33,800      │  ← VIP배지(gold) + 금색 가격
└──────────────────────┘
```

### Card Specs

| 요소 | 스타일 |
|------|--------|
| 카드 배경 | `#FFFFFF`, `border: 1px solid #E0E0E0` |
| `border-radius` | `6–8px` |
| 이미지 영역 | 정방형(1:1) 또는 4:3, 배경 `#F5F5F5` |
| 이미지 비율 | `aspect-ratio: 1/1` 권장 |
| hover shadow | `0 8px 32px rgba(0,0,0,0.10)` |
| 품절 처리 | 이미지 위 흰색 오버레이(opacity 0.7) + "품절" 텍스트 |
| VIP 가격 표시 | Gold 배지(`#C9A84C`) + 금색 텍스트 |

---

## 09 Section Patterns

### Page Section Flow

| # | 섹션 | 배경 | 높이/패딩 | 특징 |
|---|------|------|-----------|------|
| 1 | 공지/프로모 배너 스트립 | Orange / Black | h: 36–40px | full-width, 2단 배너 |
| 2 | Sticky Header | White | h: 60–72px | sticky top:0, z-index:100 |
| 3 | 메인 히어로 배너 슬라이더 | — | h: 400–600px | full-width, auto-play slider |
| 4 | Best Seller | White | padding: 64px 0 | 4-col grid |
| 5 | New Arrival | `#F5F5F5` | — | 4–6 col |
| 6 | 큐레이션 / 테마 특집 | — | — | 2-col editorial, image-heavy |
| 7 | 앱 다운로드 프로모 배너 | Dark | — | full-width, app mockup |
| 8 | CSR / 브랜드 스토리 | — | — | photo grid, emotional |
| 9 | Footer | `#0F0F1A` | — | 4-col links, award badges |

### Section Header Pattern

```
SMALL LABEL (uppercase · letter-spacing · gray)
큰 제목 텍스트                                   ← Display / H1 크기
간략한 서브카피                                   ← Body / gray
```

---

## 10 Effects & Motion

### Border Radius

| 값 | 용도 |
|----|------|
| `3px` | 배지 |
| `4px` | 버튼, 카드 |
| `8px` | 큰 카드 |
| `50%` | 아이콘 원형 |

> 페스룸은 각진 디자인 철학을 유지합니다. 최대 border-radius는 8px이며 pill 형태(50px+)는 사용하지 않습니다.

### Shadow System

| 단계 | 값 | 용도 |
|------|-----|------|
| Elevation 1 | `0 1px 4px rgba(0,0,0,0.06)` | 카드 기본 |
| Elevation 2 | `0 4px 16px rgba(0,0,0,0.09)` | 호버 상태 |
| Elevation 3 | `0 8px 32px rgba(0,0,0,0.12)` | 모달/팝업 |

### Motion Tokens

| 토큰 | 값 | 용도 |
|------|-----|------|
| `--duration-fast` | `150ms` | 버튼 hover, 아이콘 상태 변화 |
| `--duration-base` | `200ms` | 카드 hover, 색상 전환 |
| `--duration-slow` | `300ms` | 슬라이더, 드롭다운 열림/닫힘 |
| `--ease-default` | `ease` | 기본 전환 |
| `--ease-out` | `cubic-bezier(0,0,0.2,1)` | 입장 애니메이션 |
| card hover | `translateY(-4px)` | 상품 카드 마우스 오버 |
| button hover | `opacity: 0.85` | 버튼 피드백 |

---

## 11 Navigation Structure

### GNB 계층 구조

```
SHOP
  ├── ALL / NEW / BEST / COLLABO
  ├── FOR DOG
  ├── FOR CAT
  ├── 카테고리: 사료 · 간식 · 영양/건강 · 뷰티/케어 · 산책/놀이 · IoT
  └── 정기배송: 고양이 모래 · 강아지 패드 · 커스텀 믹스

VIP CENTER
  ├── VIP 혜택 안내
  ├── VIP 전용 상품
  └── 멤버십 가입

PETHROOM FRIENDS (APP)
  ├── 앱 소개
  └── 다운로드 링크

EVENT
  ├── 진행중인 이벤트
  └── 종료된 이벤트

About

Community
  ├── 후기 게시판
  └── 펫 스토리
```

---

## 12 Do's & Don'ts

### ✅ Do — 따라야 할 원칙

- 배경은 흰색 또는 연회색 계열 유지
- 오렌지는 CTA, 배지, 포인트에만 소량 사용
- 상품 이미지가 돋보이도록 카드 배경은 항상 중립적으로
- VIP 가격은 별도 골드 컬러로 항상 구분 표시
- 버튼은 4px 내외의 미니멀한 border-radius 유지
- 텍스트 굵기로 정보 계층을 명확히 구분 (900 / 700 / 400)
- 그리드 간격은 20–24px 일관 유지
- 수상 배지(Red Dot 등)는 Footer에 배치해 신뢰도 강조

### ❌ Don't — 피해야 할 패턴

- 오렌지를 텍스트 색상으로 대량 사용하지 않기
- pill 형태(border-radius 50px+) 버튼 사용 금지
- 그림자를 과도하게 사용해 무거운 느낌 주지 않기
- 배경에 패턴이나 텍스처 넣지 않기 (미니멀 유지)
- 상품 카드 내 정보를 5가지 이상 노출하지 않기
- 세리프(명조) 폰트 사용 금지
- 섹션마다 다른 배경색을 사용해 파편화하지 않기
- 모바일에서 한 줄에 상품 3개 이상 배치 금지

---

*Pethroom Design Guide · Analyzed from pethroom.com · For reference use*
