# 랜딩 템플릿 모음

배포용 저장소. 템플릿을 하나씩 추가해 포트폴리오로 쌓는 구조.

```
landing-templates/
├── index.html              ← 포트폴리오 인덱스
├── thumbs/                 ← 인덱스에 쓸 미리보기 이미지
│   └── t01.jpg
└── t01-franchise/          ← 템플릿 1
    ├── index.html
    └── images/             ← 이 템플릿의 사진
```

## 처음 한 번만

1. GitHub에서 새 저장소 생성 — 이름 `landing-templates`, Public
2. 이 폴더 전체를 업로드 (웹에서 Add file → Upload files, 폴더째 드래그하면 됨)
3. vercel.com → Add New → Project → 방금 만든 저장소 Import
4. 설정 그대로 두고 Deploy. 빌드 설정 불필요
5. 1분 뒤 `landing-templates-xxxx.vercel.app` 주소가 나옴

## 템플릿 추가할 때

1. `t02-이름/` 폴더를 만들고 `index.html` 넣기
2. `index.html`(루트)의 카드 하나를 복사해 링크를 `/t02-이름/`으로 수정
3. GitHub에 push → Vercel이 자동 배포

주소는 `사이트주소/t02-이름/` 이 됨.

## 실제 고객사 건은 따로

포트폴리오용과 고객사 납품용은 저장소를 분리할 것. 고객사 건은 `c001-고객사명` 저장소를 따로 만들고 도메인도 따로 연결.

이유는 두 가지.
- 고객사가 자기 사이트 주소 밑에 다른 업체 사례가 딸려 나오는 걸 원하지 않음
- 나중에 이관 요청이 오면 저장소째 넘기면 끝남

## 인덱스는 검색 제외

`index.html`에 `<meta name="robots" content="noindex">`를 넣어뒀음. 샘플 사이트가 검색에 잡히면 실제 브랜드로 오해받거나, 가상의 손익 숫자가 문제가 될 수 있음. 영업용으로 링크만 보내는 용도로 쓸 것.

같은 이유로 각 템플릿 페이지에도 실제 고객사 건이 아니면 noindex를 넣는 게 안전함.
