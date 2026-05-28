# 🚀 배포 가이드 (처음부터 끝까지)

GitHub Pages로 이 랜딩페이지를 배포하는 가장 쉬운 방법입니다.
**컴퓨터 한 번도 안 만져본 분이라도 30분 안에 끝낼 수 있게** 단계별로 정리했습니다.

---

## ✅ 준비물 (5분)

1. **GitHub 계정** → https://github.com/signup (무료, 이메일만 있으면 됨)
2. **이 폴더 (deploy 폴더)** → 통째로 다운로드 받아 놓기

---

## 📌 STEP 1 — GitHub에 새 저장소 만들기 (3분)

1. GitHub 로그인 후 우측 상단의 **`+` 버튼 → New repository** 클릭

2. 다음과 같이 입력
   - **Repository name** : `ai-marketing-class` (원하는 이름)
   - **Public** 선택 (Pages 무료 사용 조건)
   - **Add a README file** 은 **체크하지 말 것** (이미 README가 있음)
   - 나머지는 그대로

3. 아래쪽 초록색 **`Create repository`** 클릭

---

## 📌 STEP 2 — 파일 업로드 (5분)

1. 방금 만든 저장소 페이지에서 **`uploading an existing file`** 링크 클릭
   (또는 **Add file → Upload files**)

2. **deploy 폴더 안의 모든 것**을 끌어다 놓기
   - `index.html`
   - `images` 폴더 (통째로)
   - `.nojekyll` (숨김 파일 — Mac은 ⌘+⇧+. , Windows는 폴더 옵션에서 숨김파일 보이기)
   - `README.md`
   - `.gitignore`

3. 아래쪽 **Commit changes** 클릭

⚠️ `.nojekyll` 이 안 올라가면 사이트가 깨질 수 있으니 꼭 확인하세요.

---

## 📌 STEP 3 — GitHub Pages 켜기 (2분)

1. 저장소 상단 메뉴에서 **`Settings`** 클릭

2. 왼쪽 사이드바에서 **`Pages`** 클릭

3. **Build and deployment** 영역에서
   - **Source** : `Deploy from a branch` 선택
   - **Branch** : `main` / `/ (root)` 선택
   - **Save** 클릭

4. **1~2분 기다리기** ☕

5. 페이지 상단에 초록색 박스가 뜨면 완료!
   ```
   ✅ Your site is live at https://[사용자명].github.io/ai-marketing-class/
   ```
   이 URL이 바로 배포된 랜딩페이지 주소입니다.

---

## 📌 STEP 4 — 광고 / SNS에 뿌리기 (1분)

위에서 얻은 URL을 그대로 광고 / 카톡 / 페북 / 인스타에 공유하면 됩니다.
**카카오톡으로 공유하면 강연 사진이 자동으로 미리보기 이미지로 뜹니다.**

---

## 🔧 자주 묻는 질문

### Q1. 한국 도메인(.kr / .co.kr)을 연결하고 싶어요
가능합니다. 도메인 등록 업체(가비아, 후이즈, 카페24 등)에서 구매한 도메인을
GitHub Pages에 연결할 수 있어요.

1. GitHub 저장소 → **Settings → Pages → Custom domain** 에 도메인 입력
   (예: `event.globalselleredu.com`)

2. 도메인 등록 업체 사이트에서 **DNS 설정** 메뉴 진입

3. **CNAME 레코드** 추가
   - 호스트 / 이름 : `event` (서브도메인만 입력)
   - 값 / 대상 : `[사용자명].github.io`

4. 10분 ~ 24시간 안에 적용됨. 적용된 뒤에는 GitHub Pages 설정에서
   **`Enforce HTTPS`** 도 자동으로 체크 가능

### Q2. 페이지 내용을 수정하고 싶어요
1. GitHub에서 `index.html` 파일 클릭
2. 오른쪽 위 연필 아이콘 ✏️ 클릭
3. 수정 후 아래쪽 **Commit changes** 클릭
4. 1~2분 뒤 자동 반영

### Q3. 신청 마감되면 페이지를 어떻게 내리나요
저장소 **Settings → Pages → Source → None** 선택하면 사이트가 즉시 내려갑니다.
또는 `index.html` 을 마감 안내 페이지로 교체해도 됩니다.

### Q4. 신청 링크 (`globalselleredu.com/classes/304160`) 가 바뀌었어요
`index.html` 안에서 **3군데**의 신청 링크를 찾아 바꾸면 됩니다.
GitHub 웹 편집기의 검색 기능(`Cmd+F` / `Ctrl+F`)으로 `304160` 검색하면 빠릅니다.

### Q5. 카톡 미리보기 이미지가 안 뜨거나 옛날 이미지가 떠요
카카오톡은 한 번 캐시한 미리보기를 며칠간 보관합니다.
강제 갱신 방법 :
1. https://developers.kakao.com/tool/clear/og 접속 (카카오 디벨로퍼스 OG 캐시 초기화)
2. 본인 URL 입력 후 **초기화**

페이스북도 비슷한 도구 : https://developers.facebook.com/tools/debug/

---

## 💡 더 쉬운 대안 — 코드 안 만지고 배포

GitHub가 어려우면 다음 서비스들도 똑같이 무료로 가능합니다.

- **Netlify** (https://app.netlify.com/drop) — deploy 폴더를 끌어다 놓기만 하면 끝
- **Vercel** (https://vercel.com) — GitHub 연동으로 자동 배포
- **Cloudflare Pages** — 한국에서 속도가 가장 빠름

이 중 **Netlify Drop**이 가장 간단합니다. URL에 폴더만 끌어다 놓으면 30초 안에 배포됩니다.

---

## 🆘 막히면

GitHub 공식 한국어 문서 : https://docs.github.com/ko/pages
