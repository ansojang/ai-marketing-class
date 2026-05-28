# AI 활용 1인 마케팅 대행사 세팅 특강 — 랜딩페이지

> 네이버 바이럴 17년, 페북 광고 연 5억을 다 해본 안영신 소장의 AI 마케팅 특강 모집용 랜딩페이지

## 📅 강의 정보

- **일시** : 2026년 6월 18일 (수) 저녁 8시 ~ 10시
- **장소** : 온라인 ZOOM
- **정원** : 선착순 100명
- **참가비** : ~~30,000원~~ → **1회 한정 100% 무료 전환**
- **신청** : https://www.globalselleredu.com/classes/304160

---

## 🌐 GitHub Pages로 배포하기

### 방법 1 : 새 저장소에 그대로 올리기 (가장 간단)

1. GitHub에서 새 저장소를 만든다 (예: `ai-marketing-landing`)
2. 이 폴더의 모든 파일을 저장소에 업로드
   - `index.html`
   - `images/` 폴더 (lecture_2.jpg, lecture_3.jpg, lecture_4.jpg, lecture_hall.jpg)
   - `.nojekyll` (필수)
   - `README.md` (선택)
3. 저장소 **Settings → Pages** 메뉴 이동
4. **Source** 를 `Deploy from a branch` 로 선택
5. **Branch** 를 `main` (또는 `master`) / `/ (root)` 로 선택 후 **Save**
6. 약 1~2분 뒤 `https://[GitHub사용자명].github.io/[저장소이름]/` 에서 접속 가능

### 방법 2 : 기존 저장소의 하위 폴더로 배포

1. 기존 저장소의 `docs/` 폴더 안에 모든 파일을 넣는다
2. **Settings → Pages → Source → Branch** 에서 `main` / `/docs` 선택
3. 저장 후 동일하게 접속 가능

### 방법 3 : 커스텀 도메인 연결 (예 : event.globalselleredu.com)

1. 위 방법 1 또는 2로 먼저 배포
2. **Settings → Pages → Custom domain** 에 도메인 입력 (예: `event.globalselleredu.com`)
3. 도메인 등록 업체(가비아 / 후이즈 / Cloudflare 등)에서 DNS 설정
   - **CNAME** 레코드 추가
   - 호스트 : `event` (서브도메인)
   - 값 : `[GitHub사용자명].github.io`
4. DNS 전파 후 (보통 10분 ~ 24시간) HTTPS 자동 활성화

---

## 📁 파일 구조

```
deploy/
├── index.html          ← 메인 랜딩페이지
├── images/
│   ├── lecture_4.jpg       ← 메인 강연 사진
│   ├── lecture_hall.jpg    ← 단체 사진 (보드)
│   ├── lecture_3.jpg       ← VIP 워크샵
│   └── lecture_2.jpg       ← 강연 직전 무대
├── .nojekyll           ← GitHub Pages 빌드 우회용 (필수)
└── README.md
```

---

## ✏️ 수정 방법

### 강의 일정 / 참가비 / 정원 바꾸기

`index.html` 파일을 텍스트 에디터로 열고 다음 부분을 찾아 수정:

- **상단 띠** : `<!-- TOP STRIP -->` 영역
- **강의 정보 박스** : `<!-- COURSE INFO -->` 섹션
- **최종 정보 박스** : `<!-- FINAL MESSAGE -->` 섹션

### 신청 링크 바꾸기

`index.html`에서 `https://www.globalselleredu.com/classes/304160` 를 검색해서
새 URL로 일괄 교체. 총 3군데에 있다.

### 사진 교체

`images/` 폴더의 파일을 같은 이름으로 덮어쓰기.
사이즈는 가로 1600px 이하, JPG 권장 (500KB 이하).

---

## 🎯 SNS 공유 시 미리보기 이미지

카카오톡 / 페이스북 / 트위터로 링크 공유 시, **메인 강연 사진(`lecture_4.jpg`)** 이
자동으로 미리보기 이미지로 표시되도록 Open Graph 메타 태그가 설정되어 있다.

별도 OG 이미지를 따로 만들고 싶으면 `images/og.jpg` (1200×630px 권장)를 추가한 뒤
HTML 상단의 `og:image` 와 `twitter:image` 경로를 바꿔주면 된다.

---

## 📞 문의

- **사이트** : https://www.globalselleredu.com
- **발행** : 안영신 소장 · 글로벌셀러창업연구소
