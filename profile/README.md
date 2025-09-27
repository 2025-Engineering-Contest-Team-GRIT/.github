### <p align = center> 2025 Engineering Contest Team GRIT <p>
# 한성 길라잡이
<p align="center">
<img width="511.5" height="319.5" alt="image" src="https://github.com/user-attachments/assets/8e592816-a355-4da2-b363-63df0e86b732" />
</p>
<br>

### 배포 링크
<blockquote>https://hangil.site</blockquote>
<br>

# 서비스 개요


# Demo
### 로그인

<br><br>

### 대시보드

<br><br>

### 이수현황
<br><br>

### 시간표
<br><br>

### 졸업요건
<br><br>

### 졸업 시뮬레이션
<br><br>

### Rag 아키텍처 (로드맵 생성 과정)
<img width="605" height="272" alt="image" src="https://github.com/user-attachments/assets/ab75fb88-f2fb-41f4-a0dc-7432b065b6e7" />
<br>

**과목 데이터 → Qdrant 벡터화 → 사용자 쿼리 → 유사 과목 검색 → LLM 로드맵 생성**

**1. 데이터 준비 (Embedding & Indexing)**
- 모든 과목 정보(강의 계획서, 과목 설명 등)를 LLM이 이해할 수 있는 벡터(Vector) 로 변환합니다.
변환된 벡터들은 의미 기반 검색이 용이하도록 VectorDB에 저장(Indexing)됩니다.

**2. 연관 데이터 검색**
- 사용자의 정보와 설문조사(관심 분야 등) 또한 벡터로 변환됩니다.
VectorDB 내에서 사용자의 질의 벡터와 DB 내 과목 벡터들 간의 코사인 유사도(Cosine Similarity)를 측정하여 의미적으로 가장 관련성 높은 상위 K개의 문서를 신속하게 검색합니다.

**3. 프롬프트 구성 및 응답 생성**
- 검색된 정보는 사용자의 수강 이력, 트랙 정보 등 개인 데이터에 따라 한 번 더 필터링됩니다.
최종적으로 정제된 데이터는 로드맵 생성 규칙과 함께 LLM에 전달됩니다.
LLM은 이 컨텍스트를 바탕으로 환각(Hallucination) 현상을 최소화하여 맞춤형 로드맵을 생성합니다.

<br><br>


# 📗 API
<img width="2650" height="1016" alt="image" src="https://github.com/user-attachments/assets/5cc2df0b-7bd9-4c9c-baa0-5ebb6613abf7" />
<img width="2650" height="1382" alt="image" src="https://github.com/user-attachments/assets/b134d097-d910-4d38-af5a-3a549b330f7a" />
<img width="2650" height="1514" alt="image" src="https://github.com/user-attachments/assets/2d24e2ed-1577-43fa-9102-410210c0ad2c" />

<br><br>

# 🛠 ️System Architecture
<img width="1066" height="592" alt="image" src="https://github.com/user-attachments/assets/cd0090e1-3921-458f-a56d-c7b7cf98aea1" />

<br><br>

# 🔑 ERD
<img width="2910" height="1104" alt="image" src="https://github.com/user-attachments/assets/1d4564ff-1159-46c5-ae2f-03c8db572a71" />

<br><br>

# 💻 Tech Stack
<div align="center">
  <table>
    <tr>
      <th>Field</th>
      <th>Technology of Use</th>
    </tr>
    <tr>
      <td><b>Frontend</b></td>
      <td>
        <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
        <img src="https://img.shields.io/badge/Next-000000?style=for-the-badge&logo=next.js&logoColor=white">
        <img src="https://img.shields.io/badge/yarn-%232C8EBB.svg?&style=for-the-badge&logo=yarn&logoColor=white" />
        <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
        <img src="https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white">
        <img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white">
        <img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
        <img src="https://img.shields.io/badge/Prettier-F7B93E?style=for-the-badge&logo=prettier&logoColor=white">
        <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white">
        <img src="https://img.shields.io/badge/React%20Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white">
        <img src="https://img.shields.io/badge/Zustand-000000?style=for-the-badge&logo=zustand&logoColor=white">
        <img src="https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Backend</b></td>
      <td>
        <img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> 
        <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
        <img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">
        <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Database</b></td>
      <td>
        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
        <img src="https://img.shields.io/badge/Qdrant-EF4444?style=for-the-badge&logo=qdrant&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>AI</b></td>
      <td>
        <img src="https://img.shields.io/badge/OpenAI-74aa9c?style=for-the-badge&logo=openai&logoColor=white">
      </td>
      </td>
    </tr>
    <tr>
      <td><b>DevOps</b></td>
      <td>
        <img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white">
        <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
        <img src="https://img.shields.io/badge/Github Actions-2496ED?style=for-the-badge&logo=githubactions&logoColor=white">
        <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
        <img src="https://img.shields.io/badge/Traefik-24A1C1?style=for-the-badge&logo=Traefik%20Proxy&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>ETC</b></td>
      <td>
        <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white">
        <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white">
        <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white">
        <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
        <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black">
        <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white">
      </td>
    </tr>
  </table>
</div>
</br>

# 📂 Directory Structure
<details>
    <summary>Frontend</summary>
<pre>
<code>
📦Frontend
 ┣ 📂.git
 ┃ ┣ 📂hooks
 ┃ ┃ ┣ 📜applypatch-msg.sample
 ┃ ┃ ┣ 📜commit-msg.sample
 ┃ ┃ ┣ 📜fsmonitor-watchman.sample
 ┃ ┃ ┣ 📜post-update.sample
 ┃ ┃ ┣ 📜pre-applypatch.sample
 ┃ ┃ ┣ 📜pre-commit.sample
 ┃ ┃ ┣ 📜pre-merge-commit.sample
 ┃ ┃ ┣ 📜pre-push.sample
 ┃ ┃ ┣ 📜pre-rebase.sample
 ┃ ┃ ┣ 📜pre-receive.sample
 ┃ ┃ ┣ 📜prepare-commit-msg.sample
 ┃ ┃ ┣ 📜push-to-checkout.sample
 ┃ ┃ ┗ 📜update.sample
 ┃ ┣ 📂info
 ┃ ┃ ┗ 📜exclude
 ┃ ┣ 📂logs
 ┃ ┃ ┣ 📂refs
 ┃ ┃ ┃ ┣ 📂heads
 ┃ ┃ ┃ ┃ ┗ 📜develop
 ┃ ┃ ┃ ┗ 📂remotes
 ┃ ┃ ┃ ┃ ┗ 📂origin
 ┃ ┃ ┃ ┃ ┃ ┗ 📜HEAD
 ┃ ┃ ┗ 📜HEAD
 ┃ ┣ 📂objects
 ┃ ┃ ┣ 📂info
 ┃ ┃ ┗ 📂pack
 ┃ ┃ ┃ ┣ 📜pack-3e6ae162964f898e9555f4b541a48afd891d14f7.idx
 ┃ ┃ ┃ ┗ 📜pack-3e6ae162964f898e9555f4b541a48afd891d14f7.pack
 ┃ ┣ 📂refs
 ┃ ┃ ┣ 📂heads
 ┃ ┃ ┃ ┗ 📜develop
 ┃ ┃ ┣ 📂remotes
 ┃ ┃ ┃ ┗ 📂origin
 ┃ ┃ ┃ ┃ ┗ 📜HEAD
 ┃ ┃ ┗ 📂tags
 ┃ ┣ 📜HEAD
 ┃ ┣ 📜config
 ┃ ┣ 📜description
 ┃ ┣ 📜index
 ┃ ┗ 📜packed-refs
 ┣ 📂.github
 ┃ ┣ 📂ISSUE_TEMPLATE
 ┃ ┃ ┣ 📜📑-문서화.md
 ┃ ┃ ┣ 📜🔨-버그-해결.md
 ┃ ┃ ┣ 📜🖌️-퍼블리싱.md
 ┃ ┃ ┣ 📜🚀-기능-구현.md
 ┃ ┃ ┣ 📜🧭-환경설정.md
 ┃ ┃ ┗ 📜🧹-리팩토링.md
 ┃ ┗ 📜pull_request_template.md
 ┣ 📂.vscode
 ┃ ┣ 📜settings.json
 ┃ ┗ 📜tasks.json
 ┣ 📂public
 ┃ ┣ 📜file.svg
 ┃ ┣ 📜globe.svg
 ┃ ┣ 📜logo.svg
 ┃ ┣ 📜next.svg
 ┃ ┣ 📜vercel.svg
 ┃ ┗ 📜window.svg
 ┣ 📂src
 ┃ ┣ 📂app
 ┃ ┃ ┣ 📂(app)
 ┃ ┃ ┃ ┣ 📂completion
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂dashboard
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂graduation
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂roadmap
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂simulation
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂timetable
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┗ 📜layout.tsx
 ┃ ┃ ┣ 📂(auth)
 ┃ ┃ ┃ ┣ 📂login
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┣ 📂onboarding
 ┃ ┃ ┃ ┃ ┗ 📜page.tsx
 ┃ ┃ ┃ ┗ 📜layout.tsx
 ┃ ┃ ┣ 📜favicon.ico
 ┃ ┃ ┣ 📜globals.css
 ┃ ┃ ┣ 📜layout.tsx
 ┃ ┃ ┗ 📜page.tsx
 ┃ ┣ 📂components
 ┃ ┃ ┣ 📂client
 ┃ ┃ ┃ ┣ 📂wrapper
 ┃ ┃ ┃ ┃ ┣ 📜HeaderClientWrapper.tsx
 ┃ ┃ ┃ ┃ ┗ 📜LoginClientWrapper.tsx
 ┃ ┃ ┃ ┣ 📜CompletionPageClient.tsx
 ┃ ┃ ┃ ┣ 📜DashboardPageClient.tsx
 ┃ ┃ ┃ ┣ 📜ErrorBoundary.tsx
 ┃ ┃ ┃ ┣ 📜GraduationPageClient.tsx
 ┃ ┃ ┃ ┣ 📜Navigation.tsx
 ┃ ┃ ┃ ┣ 📜RoadmapPageClient.tsx
 ┃ ┃ ┃ ┣ 📜SimulationPageClient.tsx
 ┃ ┃ ┃ ┗ 📜TimetablePageClient.tsx
 ┃ ┃ ┣ 📂server
 ┃ ┃ ┃ ┗ 📜Layout.tsx
 ┃ ┃ ┣ 📂views
 ┃ ┃ ┃ ┣ 📜CompletionStatusView.tsx
 ┃ ┃ ┃ ┣ 📜DashboardView.tsx
 ┃ ┃ ┃ ┣ 📜GraduationView.tsx
 ┃ ┃ ┃ ┣ 📜LoginScreen.tsx
 ┃ ┃ ┃ ┣ 📜OnboardingScreen.tsx
 ┃ ┃ ┃ ┣ 📜RoadmapView.tsx
 ┃ ┃ ┃ ┣ 📜SimulationView.tsx
 ┃ ┃ ┃ ┣ 📜TimetableView.tsx
 ┃ ┃ ┃ ┗ 📜index.ts
 ┃ ┃ ┣ 📜Button.tsx
 ┃ ┃ ┣ 📜ConfirmationModal.tsx
 ┃ ┃ ┣ 📜CourseCard.tsx
 ┃ ┃ ┣ 📜OnboardingRestartModal.tsx
 ┃ ┃ ┣ 📜PrivacyPolicyModal.tsx
 ┃ ┃ ┣ 📜ProgressBar.tsx
 ┃ ┃ ┣ 📜Toast.tsx
 ┃ ┃ ┣ 📜Toggle.tsx
 ┃ ┃ ┣ 📜animations.ts
 ┃ ┃ ┗ 📜common.tsx
 ┃ ┣ 📂data
 ┃ ┃ ┗ 📜courseData.ts
 ┃ ┣ 📂hooks
 ┃ ┃ ┣ 📜useData.ts
 ┃ ┃ ┗ 📜useStore.ts
 ┃ ┣ 📂providers
 ┃ ┃ ┗ 📜QueryProvider.tsx
 ┃ ┣ 📂services
 ┃ ┃ ┣ 📜api.ts
 ┃ ┃ ┣ 📜authService.ts
 ┃ ┃ ┗ 📜modifyService.ts
 ┃ ┣ 📂store
 ┃ ┃ ┗ 📜index.ts
 ┃ ┣ 📂styles
 ┃ ┃ ┗ 📜theme.ts
 ┃ ┣ 📂views
 ┃ ┃ ┣ 📜DashboardView.tsx
 ┃ ┃ ┣ 📜LoginScreen.tsx
 ┃ ┃ ┗ 📜OnboardingScreen.tsx
 ┃ ┗ 📜types.ts
 ┣ 📜.eslintignore
 ┣ 📜.eslintrc.json
 ┣ 📜.gitignore
 ┣ 📜.prettierignore
 ┣ 📜.prettierrc
 ┣ 📜README.md
 ┣ 📜eslint.config.mjs
 ┣ 📜jest.config.js
 ┣ 📜jest.setup.js
 ┣ 📜main.sql
 ┣ 📜main.vuerd.json
 ┣ 📜next.config.ts
 ┣ 📜package-lock.json
 ┣ 📜package.json
 ┣ 📜postcss.config.mjs
 ┣ 📜temp.vuerd.json
 ┗ 📜tsconfig.json

  </code>
</pre>
</details>

<details>
    <summary>Backend</summary>
<pre>
<code>

📦src
 ┣ 📂main
 ┃ ┣ 📂java
 ┃ ┃ ┗ 📂grit
 ┃ ┃ ┃ ┗ 📂guidance
 ┃ ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┃ ┣ 📂course
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CourseAdminController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CourseDataDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂entity
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Course.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CoursePrerequisite.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseType.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Semester.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Track.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜TrackRequirement.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CoursePrerequisiteRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TrackRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜TrackRequirementRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseDescriptionCrawlingService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TrackRequirementService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜TrackService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂graduation
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜GraduationController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CertificationStatusDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CrawlingGraduationDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DashboardResponseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DetailedCreditDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationPlanRequestDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationResponseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜TrackProgressDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂entity
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CrawlingGraduation.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CrawlingGraduationRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜GraduationService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂roadmap
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜RoadmapController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseRecommendationRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜RoadmapDataDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜RoadmapResponseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SearchRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SemesterDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂entity
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜RecommendedCourse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜QdrantRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜RecommendedCourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseEmbeddingService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LlmRoadmapService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜RecommendedCourseService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜RoadmapService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂simulation
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SimulationController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationPlanRequestDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SimulationDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂entity
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationPlan.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜GraduationPlanCourse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationPlanCourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜GraduationPlanRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SimulationService.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📂user
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂controller
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CrawlingController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DashboardController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourseController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserSyncController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜AcademicStatusDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CareerGoalDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CourseGradeResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DashboardDataDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DashboardResponseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜ErrorResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourseRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourseResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜HansungDataResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MajorCreditDetail.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MajorCreditTotal.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MajorRequiredCreditsResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜NextSemesterCourseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SemesterGradeResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableDataDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableDetailDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableEventDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TotalGradeResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserCourseDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserInfoDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserInfoResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserSyncRequestDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UserTrackDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂entity
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CompletedCourse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CompletedGrade.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜EnrolledCourse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationRequirement.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Setting.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TrackType.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserTrack.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜Users.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CompletedCourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜EnrolledCourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourseRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜GraduationRequirementRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserTrackRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UsersRepository.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CrawlingConditionService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜DashboardService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FavoriteCourseService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜LoginService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜TimetableService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserAcademicInfoSyncService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserCourseService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜UserDetailsServiceImpl.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UsersCrawlingService.java
 ┃ ┃ ┃ ┃ ┣ 📂global
 ┃ ┃ ┃ ┃ ┃ ┣ 📂common
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📂response
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜ApiResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜BaseEntity.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SystemData.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SystemDataRepository.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂config
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜QdrantConfig.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜SecurityConfig.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SwaggerConfig.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📂jwt
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜JwtAuthenticationFilter.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜JwtService.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜JwtToken.java
 ┃ ┃ ┃ ┃ ┗ 📜GuidanceApplication.java
 ┃ ┗ 📂resources
 ┃ ┃ ┣ 📂data
 ┃ ┃ ┃ ┗ 📜courses.json
 ┃ ┃ ┣ 📜application-dev.yml
 ┃ ┃ ┣ 📜application-local.yml
 ┃ ┃ ┗ 📜application.yml
 ┗ 📂test
 ┃ ┗ 📂java
 ┃ ┃ ┗ 📂grit
 ┃ ┃ ┃ ┗ 📂guidance
 ┃ ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┃ ┣ 📂roadmap
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CourseEmbeddingServiceTest.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📂user
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜UsersCrawlingServiceTest.java
 ┃ ┃ ┃ ┃ ┗ 📜GuidanceApplicationTests.java

 </code>
</pre>
</details>

# 🚀 How to Start
#### 1. Clone The Repository
```
https://github.com/2025-Engineering-Contest-Team-GRIT/Frontend.git
https://github.com/2025-Engineering-Contest-Team-GRIT/Backend.git
```
#### 2. ENV Setting
- Backend/.env
```
POSTGRES_DB=
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_URL=
SPRING_PROFILES_ACTIVE=
OPENAI_API_KEY=
```
#### 3. Run Docker
```
docker-compose up --build
```
### Install
```
yarn install
```

### Run
```
yarn run dev
```
<br>

## 👥 Member
| Name | 최재현 | 김환희 | 변정원 | 김지훈 |
|:---:|:---:|:---:|:---:|:---:|
| Role | Team Leader, <br>Backend | Backend, DevOps | Backend | Frontend, Design |
| GitHub | <a href="https://github.com/MacArthur17"><img src="http://img.shields.io/badge/MacArthur17-green?style=social&logo=github"/></a> | <a href="https://github.com/hwanh2"><img src="http://img.shields.io/badge/hwanh2-green?style=social&logo=github"/></a> | <a href="https://github.com/Yeeyahou"><img src="http://img.shields.io/badge/Yeeyahou-green?style=social&logo=github"/></a> | <a href="https://github.com/urous3814"><img src="http://img.shields.io/badge/urous3814-green?style=social&logo=github"/></a> |

