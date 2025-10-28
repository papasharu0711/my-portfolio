# 프로젝트 포트폴리오 랜딩 페이지

Vercel로 배포 가능한 현대적인 프로젝트 포트폴리오 사이트입니다.

## ✨ 주요 특징

### 🎨 Modern UX/UI Design
- **Lucide Icons**: 이모티콘 대신 전문적인 아이콘 라이브러리 사용
- **카드 썸네일**: 각 프로젝트에 시각적 썸네일 영역
- **상태 표시**: Live/Beta 등 프로젝트 상태를 명확하게 표시
- **카테고리 시스템**: Game, Creative, Utility 등 프로젝트 분류
- **필터 탭**: 프로젝트를 카테고리별로 필터링 (향후 JavaScript로 동작 구현 가능)

### 📐 정보 구조 (Information Architecture)
- **명확한 계층**: 카테고리 > 제목 > 설명 > 기술스택 순으로 정보 배치
- **일관된 레이아웃**: 모든 카드가 동일한 구조로 스캔하기 쉬움
- **Footer 영역**: 프로젝트와 연락처 정보를 명확히 구분

### 🎯 UX 개선 사항
- **호버 피드백**: 마이크로 인터랙션으로 클릭 가능한 요소 강조
- **상태 표시**: 프로젝트가 라이브 상태인지 개발 중인지 한눈에 확인
- **외부 링크 표시**: "View" 버튼과 화살표 아이콘으로 외부 링크 명시
- **반응형 디자인**: 모든 기기에서 최적화된 경험

### 🎨 시각적 디자인
- **다크 테마**: 눈의 피로를 줄이는 세련된 다크 배경
- **미묘한 그라데이션**: 배경에 은은한 컬러 포인트
- **글래스모피즘**: 반투명 카드와 블러 효과
- **커스텀 스크롤바**: 전체적인 디자인과 조화로운 스크롤바

## 🚀 Vercel에 배포하는 방법

### 1. GitHub 저장소 생성
1. GitHub에서 새 저장소를 생성합니다
2. 이 파일들을 저장소에 업로드합니다:
   - `index.html`
   - `vercel.json`

### 2. Vercel에서 배포
1. [Vercel](https://vercel.com)에 접속하여 로그인
2. "New Project" 클릭
3. GitHub 저장소 연결
4. 자동으로 배포가 시작됩니다!

### 또는 Vercel CLI 사용
```bash
npm i -g vercel
vercel
```

## ✏️ 프로젝트 정보 수정하기

`index.html` 파일을 열어서 다음 부분들을 수정하세요:

### 1. 헤더 정보
```html
<h1>Projects</h1>
<p>Explore my latest work and experiments</p>
```

### 2. 각 프로젝트 카드
```html
<a href="실제프로젝트주소.vercel.app" class="project-card" target="_blank">
    <div class="project-thumbnail">
        <i data-lucide="gamepad-2" class="project-icon-large"></i>  <!-- 아이콘 변경 -->
    </div>
    <div class="project-content">
        <div class="project-header">
            <div class="project-title-wrapper">
                <div class="project-category">Game</div>  <!-- 카테고리 변경 -->
                <h3 class="project-title">프로젝트 이름</h3>  <!-- 제목 변경 -->
            </div>
            <div class="project-status status-live">  <!-- status-live 또는 status-progress -->
                <span class="status-dot"></span>
                Live  <!-- Live 또는 Beta -->
            </div>
        </div>
        <p class="project-description">
            프로젝트 설명을 여기에 작성하세요.
        </p>
        <div class="project-footer">
            <div class="project-tech">
                <span class="tech-tag">JavaScript</span>  <!-- 기술스택 변경 -->
            </div>
        </div>
    </div>
</a>
```

### 3. 아이콘 변경
Lucide 아이콘 목록: https://lucide.dev/icons/
```html
<i data-lucide="아이콘이름" class="project-icon-large"></i>
```

사용 가능한 아이콘 예시:
- `gamepad-2` - 게임
- `palette` - 디자인/크리에이티브
- `code-2` - 코딩 프로젝트
- `smartphone` - 모바일 앱
- `globe` - 웹사이트
- `database` - 백엔드
- `sparkles` - 특별한 프로젝트
- `rocket` - 런칭 프로젝트

### 4. 상태 변경
- `status-live`: 초록색 (라이브 상태)
- `status-progress`: 노란색 (개발 중/베타)

### 5. 푸터 정보
```html
<a href="https://github.com/yourusername" class="footer-link" target="_blank">
    <i data-lucide="github"></i>
    <span>GitHub</span>
</a>
```

## 🎨 커스터마이징

### 색상 변경
`<style>` 태그 안에서 주요 색상 변경:

```css
/* 배경 그라데이션 */
background: 
    radial-gradient(circle at 20% 50%, rgba(99, 102, 241, 0.1) 0%, transparent 50%);

/* Live 상태 색상 */
.status-live {
    background: rgba(16, 185, 129, 0.1);
    color: #34d399;
}

/* Beta 상태 색상 */
.status-progress {
    background: rgba(251, 191, 36, 0.1);
    color: #fbbf24;
}
```

### 프로젝트 카드 추가/삭제
`.projects-grid` 안에 카드를 추가하거나 삭제하세요.

### 필터 탭 커스터마이징
```html
<div class="filter-tabs">
    <div class="filter-tab active">All Projects</div>
    <div class="filter-tab">Games</div>
    <div class="filter-tab">Web Apps</div>
    <!-- 더 추가 가능 -->
</div>
```

## 📱 반응형 디자인
- **데스크톱**: 3열 그리드
- **태블릿**: 2열 그리드
- **모바일**: 1열 그리드

## 🌟 디자인 시스템

### 색상 팔레트
- 배경: `#0a0a0a`
- 텍스트 (주요): `#ffffff`
- 텍스트 (보조): `#9ca3af`
- 텍스트 (비활성): `#6b7280`
- 카드 배경: `rgba(255, 255, 255, 0.02)`
- 경계선: `rgba(255, 255, 255, 0.06)`

### 타이포그래피
- 헤딩: SF Pro Display, -apple-system
- 본문: 0.9375rem (15px)
- 작은 텍스트: 0.75rem (12px)

## 🎯 접근성
- 충분한 색상 대비
- 호버/포커스 상태 명확
- 키보드 내비게이션 지원
- 의미있는 HTML 구조

## 🔧 향후 개선 가능 사항
- JavaScript로 필터 기능 구현
- 프로젝트 검색 기능
- 다크/라이트 테마 토글
- 애니메이션 효과 추가
- 프로젝트 썸네일 이미지 추가
