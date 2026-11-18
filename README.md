# DongMyeongUniv
20261118

## 우리 가게 업무에 쓸 AI 스킬 추천 (한눈에 보기)

> 스킬 = AI 비서에게 특정 업무 요령을 알려 주는 "업무 매뉴얼"입니다.
> 아직 **아무것도 설치하지 않았습니다.** 고르신 뒤에 설치합니다.

### ✅ 꼭 추천 (6개, 한 번에 설치 가능)

| 순서 | 업무 단계 | 스킬 이름 | 이럴 때 써요 | 사용자 수 | 안전성 |
|:-:|---|---|---|--:|:-:|
| 1 | 제품 정보 정리 | product-marketing | 우리 제품의 장점·주요 고객·말투를 **기준 문서 하나로** 정리할 때 (나머지 스킬이 이 문서를 참고해요) | 9만 9천 | 🟢 |
| 2 | 고객 피드백 분석 | customer-research | 리뷰·문의를 모아 **"고객이 진짜 원하는 것"**을 찾을 때 | 12만 9천 | 🟡 |
| 3 | 콘텐츠 기획 | content-strategy | **무엇을, 언제 올릴지** 콘텐츠 계획표를 짤 때 | 18만 | 🟡 |
| 4 | 글쓰기 | copywriting | 상세페이지·소개글 **문구를 새로 쓸 때** | 25만 9천 | 🟢 |
| 5 | 글 다듬기 | copy-editing | 이미 쓴 글을 **읽기 쉽게 고칠 때** | 16만 4천 | 🟢 |
| 6 | SNS 발행 준비 | social | 인스타그램·블로그 등 **채널별 게시물 초안**과 일정을 만들 때 (자동 게시 안 함) | 10만 1천 | 🟡 |

- 만든 곳: coreyhaines31/marketingskills (GitHub 별 6만 1천 개, 무료 공개 라이선스)

### ➕ 필요하면 추가 (3개, 해외 쇼핑몰용)

| 스킬 이름 | 이럴 때 써요 | 사용자 수 | 안전성 |
|---|---|--:|:-:|
| product-description-generator | 상품명·특징·상세설명·검색 키워드를 한 번에 만들 때 | 1천 7백 | 🟡 |
| product-review-analysis | 리뷰의 불만·칭찬 패턴을 정리할 때 | 1천 5백 | 🟡 |
| ecommerce-content-marketing | 리뷰와 경쟁사를 참고해 쇼핑몰 콘텐츠 계획을 세울 때 | 1천 4백 | 🟡 |

- 만든 곳: nexscope-ai/eCommerce-Skills (GitHub 별 1천 5백 개). 아마존·엣시 같은 해외 마켓 기준이고 자사 홍보 문구가 붙어 있어요.

### ❌ 추천하지 않음

| 스킬 | 이유 |
|---|---|
| 한국어 맞춤법 검사 (korean-spell-check) | 글을 외부 사이트로 보내는데, 그 사이트가 **"비상업적 용도만 무료"**라서 가게 업무용으로는 맞지 않아요 |
| 브랜드 평판 모니터링 (apify) | 보안 검사 1건 실패, 별도 유료 계정 필요 |
| 사용자 수가 매우 적은 스킬들 | 검증이 부족해요 (100명 미만) |

### 안전성 표시 읽는 법
- 🟢 보안 검사 3종(Gen Agent Trust Hub·Socket·Snyk) 모두 통과
- 🟡 "주의" 1건. **바이러스나 악성 코드라는 뜻은 아닙니다.** 인터넷 글을 읽을 때 그 글에 엉뚱한 지시가 섞일 수 있다는 일반적인 경고예요. 리뷰·문의 내용을 **직접 붙여 넣어 쓰면** 위험이 거의 없습니다.
- 사용자 수와 안전성은 2026-11-18 skills.sh 화면 기준입니다(추정치 없음).

### 설치 명령 (승인하시면 실행)
```bash
npx skills add coreyhaines31/marketingskills --skill product-marketing customer-research content-strategy copywriting copy-editing social
```
```bash
npx skills add nexscope-ai/eCommerce-Skills --skill product-description-generator product-review-analysis ecommerce-content-marketing
```

자세한 검토 내용(원본 저장소 평판, 각 스킬의 권한, 보안 경고 원문)은 [docs/skill-review-detail.md](docs/skill-review-detail.md)에 있습니다.
