**모든 답변은 한국어로만 한다.**

# landing-templates

랜딩페이지 제작 대행용 템플릿 모음 저장소.

## 목적
업종별 랜딩페이지 샘플을 하나씩 쌓아 영업용 포트폴리오로 씀.
실제 고객사 납품 건은 이 저장소가 아니라 `c001-고객사명` 형태로 따로 만든다.

## 구조
```
index.html              포트폴리오 인덱스 (noindex 처리됨)
thumbs/                 인덱스 카드용 미리보기 이미지
t01-franchise/          템플릿 1 · 요식업 프랜차이즈 가맹모집
  index.html
  images/               이 템플릿의 사진
```

## 기술
- 빌드 도구 없음. 순수 HTML 한 파일 + 인라인 CSS/JS
- 외부 의존: Pretendard(jsdelivr), Noto Serif KR(Google Fonts)
- 폼 전송: Formspree
- 지도: 카카오맵 (API 키 필요, 미적용 상태)
- 배포: Vercel, GitHub push 시 자동 배포

## 작업 규칙
- `═══ 교체 N ═══` 주석은 고객사별로 갈아끼울 지점 표시임. 지우지 말 것
- 이미지는 `images/` 폴더에 정해진 파일명으로 넣으면 자동 반영됨.
  파일이 없으면 회색 안내 자리가 보이고, 있으면 사진이 덮는 구조
- 애니메이션은 `prefers-reduced-motion`에서 전부 꺼지도록 되어 있음. 유지할 것
- 가맹사업법 관련 문구(14일 숙려기간, 정보공개서 등록번호, 개인정보 동의 체크박스)는
  삭제 금지. 자세한 내용은 템플릿-사용법.md 참고

## 첫 작업
이 폴더를 git 저장소로 만들고 GitHub에 올린 뒤 Vercel에 연결한다.
저장소 이름 `landing-templates`, Public.
