# GitHub Repository Explorer with Multi-language Support

## 📌 과제 개요
**목표:**
사용자가 입력한 GitHub 사용자명을 기반으로 해당 사용자의 repository 목록을 조회하고, 상세 정보를 확인하는 웹 애플리케이션을 개발합니다.

**⏳ 기간:** 3일  
**🛠 필수 기술 스택:**  
- Next.js (App Router 활용)  
- React.js (Function Component + Hooks)  
- TypeScript  
- 다국어 지원 (next-i18next)  
- 인피니티 스크롤  
- API 활용 (GitHub REST API)  
- Jest / React Testing Library  
- Storybook  
- CSS-in-JS (TailwindCSS or styled-components)

---

## ✅ 요구 사항

### 1️⃣ 메인 페이지: GitHub 사용자 검색
- 사용자가 **GitHub 사용자명**을 입력하면 해당 사용자의 repository 목록을 조회합니다.
- API: `https://api.github.com/users/{username}/repos`
- 검색 결과 목록을 **무한 스크롤(Infinite Scroll)** 방식으로 구현합니다.
- 목록에서 다음 정보를 표시합니다:
  - Repository 이름
  - Description
  - Star 개수 ⭐
  - Last Updated 날짜  
- 필터 및 정렬 기능을 제공합니다:
  - **필터**: Language(JavaScript, TypeScript, Python 등)
  - **정렬**: 최근 업데이트 순, 별점 많은 순

### 2️⃣ Repository 상세 페이지
- 사용자가 특정 repository를 클릭하면 상세 정보를 확인할 수 있습니다.
- API: `https://api.github.com/repos/{username}/{repo}`
- 상세 정보:
  - Repository 이름
  - 설명
  - Star ⭐, Fork 🍴 개수
  - Primary language
  - Open Issues 수
  - 링크: GitHub 페이지로 이동

### 3️⃣ 다국어 지원 (i18n)
- **next-i18next** 라이브러리를 사용하여 **한국어 / 영어** 다국어 지원을 구현합니다.
- `i18n.json` 파일을 만들어 다국어 텍스트를 관리합니다.
- 기본 언어는 브라우저 설정을 기반으로 자동 선택됩니다.
- 사용자는 헤더에서 언어를 변경할 수 있습니다.

### 4️⃣ UI 컴포넌트 및 Storybook
- 검색 바, Repository 리스트, Repository 상세 컴포넌트를 **Storybook**으로 문서화합니다.
- Storybook에서 다국어 UI 변화를 미리 볼 수 있도록 설정합니다.

### 5️⃣ API 에러 처리 및 UX 개선
- API 요청이 실패할 경우, 적절한 **에러 메시지**를 보여줍니다.
- 로딩 중인 상태에서 **스켈레톤 UI**를 표시합니다.

### 6️⃣ 테스트 코드 작성
- **Jest / React Testing Library**를 사용하여 주요 기능을 테스트합니다.
  - **API 응답을 Mocking**하여 테스트 진행
  - 다국어 텍스트가 정상적으로 적용되는지 테스트
  - UI 컴포넌트 단위 테스트

---

## 🌟 보너스 (Optional)
- **다크 모드 지원**: `useTheme`을 활용하여 Light / Dark 모드를 지원하면 가산점 부여.
- **PWA 지원**: 웹 앱을 오프라인에서 사용할 수 있도록 PWA 기능 추가.

---

## 🎯 평가 기준
| 평가 항목 | 설명 |
|-----------|--------------------------------|
| **기능 구현력** | 요구 사항을 정확히 구현했는가? |
| **코드 품질** | 코드가 가독성이 높고 유지보수하기 쉬운가? |
| **API 사용 능력** | GitHub API를 적절히 활용했는가? |
| **다국어 지원** | next-i18next를 활용해 정상적으로 다국어가 적용되었는가? |
| **무한 스크롤** | 인피니티 스크롤을 원활하게 구현했는가? |
| **테스트 코드** | Jest / RTL을 활용해 테스트가 작성되었는가? |
| **스토리북** | UI 컴포넌트를 분리하여 Storybook을 작성했는가? |
| **UX/UI** | 사용자 경험을 고려한 UI/UX를 구현했는가? |

---

## 🚀 제출 방법
1. **GitHub Repository 제출**
   - README.md 포함 (설치 방법, 실행 방법, 기술 스택 설명)
   - `main` 브랜치에 최종 코드 업로드

2. **배포 (선택)**
   - 가능하면 **Vercel** 또는 **Netlify**에 배포하여 URL 공유

---

## 📌 예제 레퍼런스
1. **next-i18next 다국어 지원 예제**  
   - [GitHub Repository](https://github.com/isaachinman/next-i18next)  
   - [공식 문서](https://next-i18next.com/)  

2. **인피니티 스크롤 구현 예제**  
   - [React Infinite Scroll](https://github.com/ankeetmaini/react-infinite-scroll-component)  

3. **Storybook 설정 가이드**  
   - [Storybook 공식 문서](https://storybook.js.org/docs/react/get-started/introduction)  

4. **GitHub API 문서**  
   - [GitHub REST API](https://docs.github.com/en/rest)
