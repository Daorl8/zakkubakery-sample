# STRUCTURE · zakkubakery-sample

```
zakkubakery-sample/
├─ index.html              단일 파일 (CSS·JS 인라인)
├─ wrangler.toml           name = zakkubakery-sample → zakkubakery-sample.lgt3232.workers.dev
├─ .assetsignore           img/ · 문서 · index_*.html · _deploy · 투명 png 원본 배포 제외
├─ zk-gowun-400/700.woff2  제목 (고운바탕, 사용 글자만 → 글자 추가 시 재생성)
├─ zk-pretendard.woff2     본문 (Pretendard 400–700, 사용 글자만)
├─ zk-bear.webp            히어로 곰돌이 (투명) · zk-bear.png 원본
├─ zk-logo.webp            헤더 · 푸터 로고 (투명) · zk-logo.png 원본
├─ zk-*.webp               사진 14장 (시그니처 3 · 메뉴 8 · 매일 3 · 주문 1, 일부 겹침 없음)
├─ favicon.png / og-zakku.jpg
├─ img/                    다올 제공 원본 113장 (배포 제외)
└─ CHANGELOG.md / STRUCTURE.md
```

## 섹션 순서
헤더 → 히어로 → `#signature` → `#menu`(흰 면) → Every Day → `#order` → `#visit`(흰 면) → 푸터 + 모바일 `.quick` 하단 바(스마트스토어 · 카카오톡 · 인스타그램).

## 링크 수정
스마트스토어 `smartstore.naver.com/d_super` · 카카오톡 `pf.kakao.com/_tLrhK/chat` · 인스타 `instagram.com/zakku_bakery`. 각각 히어로 버튼 · Order 목록 · 모바일 하단 바 · head JSON-LD sameAs에 있음(카톡은 Visit 버튼에도).

## 영업시간 수정 (4곳)
히어로 `.hours` · Visit `.info` · 푸터 `.meta` · head JSON-LD.

## 색 규칙
바탕 · 선은 중성(R=G=B). 노랑 `--yel`은 버튼 · 시그니처 태그에만. 곰돌이는 히어로 1번 + 로고만.

## 폰트 재생성
`pyftsubset … --name-IDs='*' --name-languages='*' --name-legacy` (LESSONS §24). Pretendard는 instancer로 400–700 자른 뒤 서브셋.
