# 소상공인(자체 제조·판매)용 에이전트 스킬 후보 검토

검토일: 2026-11-18 · 상태: **후보 정리만 완료 (설치·게시·발송 없음)**

## 검증 방법
| 항목 | 방법 | 결과 |
|---|---|---|
| find-skills 검색 | find-skills가 쓰는 skills.sh 검색 API(`/api/search`)를 같은 방식으로 호출. 원본 응답은 `docs/data/s_*.json`, `docs/data/c_*.json` 등에 보관 | 확인 |
| 설치 수·처음 등록일·보안 감사 | skills.sh 스킬 상세 페이지 (`docs/data/pages/`), Snyk 감사 상세 (`docs/data/audits/`) | 확인 |
| 원본 저장소 평판 | github.com 저장소 페이지 + skills.sh 표시 스타 수 | 확인 |
| SKILL.md·권한 | 저장소를 직접 내려받아 SKILL.md, 동봉 스크립트, 외부 접속·게시 지시를 검사 | 확인 |

수치는 모두 2026-11-18에 화면에 표시된 값이며(K = 천, M = 백만), 추정한 값은 없습니다.

## 추천 (권장 세트) — coreyhaines31/marketingskills
저장소: GitHub 스타 61.1k · 포크 8.9k · 커밋 1,470 · MIT · 최근 커밋 2026-11-17

| 단계 | 스킬 | skills.sh 설치 수 | 처음 등록 | 보안 감사 (Trust Hub / Socket / Snyk) | 권한·동작 |
|---|---|---|---|---|---|
| 제품 정보 정리 | product-marketing | 99.2K | 2026-05-14 | 통과 / 통과 / 통과 | `.agents/product-marketing.md`를 만들고 수정만 함. 스크립트·외부 접속 없음 |
| 고객 피드백 분석 | customer-research | 129.2K | 2026-03-28 | 통과 / 통과 / **경고** | 스크립트 없음. 경고(W011, 위험도 0.30): 리뷰 사이트나 커뮤니티 글을 읽을 때 생기는 간접 프롬프트 주입 위험 |
| 콘텐츠 기획 | content-strategy | 180.5K | 2026-01-26 | 통과 / 통과 / **경고** | 스크립트 없음. 경고(W011, 0.10): 웹 검색으로 주제를 찾을 때 외부 글을 읽음 |
| 발행 준비 | copywriting | 259.0K | 2026-01-19 | 통과 / 통과 / 통과 | 스크립트·외부 접속 없음 |
| 발행 준비 | copy-editing | 164.7K | 2026-01-19 | 통과 / 통과 / 통과 | 스크립트·외부 접속 없음 |
| 발행 준비 | social | 101.6K | 2026-05-14 | 통과 / 통과 / **경고** | 경고(W011, 0.30): 참고 문서의 curl 예시가 Reddit·HN·Bluesky 공개 피드를 읽음. 본문에 "명시적 승인 없이 자동 게시 금지"가 있음 |

## 선택 — nexscope-ai/eCommerce-Skills
저장소: GitHub 스타 1.5k · 포크 189 · 커밋 124 · MIT · 최근 커밋 2026-11-11

| 스킬 | 설치 수 | 보안 감사 | 비고 |
|---|---|---|---|
| product-description-generator | 1.7K | 통과 / 통과 / **경고** | 경쟁사 페이지를 웹으로 읽음(W011). SKILL.md 안에 다른 스킬 설치 명령이 있음(W012). 해외 마켓 기준 |
| product-review-analysis | 1.5K | 통과 / 통과 / **경고** | 리뷰를 직접 넣어 주면 외부 접속 없이 동작. 자사 유료 서비스 홍보 문구 있음 |
| ecommerce-content-marketing | 1.4K | 통과 / 통과 / **경고** | 웹 검색·페이지 읽기를 많이 씀(W011) |

## 보류·제외
| 스킬 | 설치 수 | 사유 |
|---|---|---|
| refoundai/lenny-skills · analyzing-user-feedback | 2.7K | 감사 모두 통과. 다만 원칙 인용 위주로 80줄 분량이라 실무 절차가 얕음. 저장소 커밋 4개 |
| nomadamas/k-skill · korean-spell-check | 13.3K | 저장소 스타 8.4K. 실제 지시문을 실행할 때마다 npm(`@nomadamas/k-skill@0`)에서 받아옴(Snyk W012). 교정 원문을 외부 서비스(nara-speller.co.kr)로 보냄. 스킬 문서에 그 서비스가 "비상업적 용도 / 개인·학생만 무료"라고 적혀 있어 **사업 용도에 맞지 않음** |
| nomadamas/k-skill · korean-character-count | 12.2K | 원격 패키지 실행 경고(W012, 위험도 0.70) |
| apify/agent-skills · apify-brand-reputation-monitoring | 2.5K | Gen Agent Trust Hub **실패**. Apify 계정이 필요함 |
| finsilabs/awesome-ecommerce-skills · product-content-enrichment | 96 | 설치 수 100 미만, 저장소 스타 65 |
| alpoxdev/hypercore-business · korean-product-detail-page | 7 | 설치 수가 너무 적음 |
| "social media" 검색 상위의 `*/superpowers/ai-*-generation` | 약 60만~100만 | 서로 다른 소유자 여러 곳이 같은 이름의 복제본을 올렸고 설치 수가 비정상적으로 큼. 신뢰하기 어려워 제외 |
| anthropics/skills · xlsx, docx | — | 이 세션에 이미 같은 기능이 있음 |

참고: 한국 판매 채널(스마트스토어 등)에 특화된 스킬 중 기준(설치 수 1K 이상, 감사 통과)을 만족하는 것은 찾지 못함.

## 설치 명령 (실행하지 않음 · 승인 후 실행)
```bash
npx skills add coreyhaines31/marketingskills --skill product-marketing customer-research content-strategy copywriting copy-editing social
```
```bash
npx skills add nexscope-ai/eCommerce-Skills --skill product-description-generator product-review-analysis ecommerce-content-marketing
```
- `-g`를 붙이면 사용자 전역에 설치하고, 붙이지 않으면 현재 프로젝트에 설치함.
- CLI 소스(`src/add.ts`)를 보면 AI 에이전트가 실행할 때는 확인 질문(`-y`)이 자동으로 생략됨. 그래서 설치할 목록을 먼저 승인해야 함.
- 여러 스킬을 지정하는 `--skill a b c` 문법은 CLI 테스트 코드에서 확인함.
