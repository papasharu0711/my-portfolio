# 🎯 프로젝트 쉽게 수정하는 방법

이제 **한 곳만 수정하면** 모든 프로젝트가 자동으로 업데이트됩니다!

---

## ✏️ 프로젝트 정보 수정하기

### 1️⃣ index.html 파일 열기
GitHub에서 파일을 클릭하고 연필 아이콘(Edit) 클릭

### 2️⃣ JavaScript 배열 찾기
파일 맨 아래쪽에 이 부분을 찾으세요:

```javascript
// ====================================
// 🎯 여기서 프로젝트 정보를 쉽게 수정하세요!
// ====================================
const projects = [
    {
        title: "게임 프로젝트 1",
        category: "Game",
        description: "재미있는 웹 기반 게임입니다...",
        url: "https://your-game-project.vercel.app",
        icon: "gamepad-2",
        status: "live",
        tags: ["JavaScript", "HTML5", "CSS3"]
    },
    // ... 더 많은 프로젝트들
];
```

### 3️⃣ 정보 수정하기

각 프로젝트는 다음 정보를 가지고 있습니다:

```javascript
{
    title: "프로젝트 제목",           // 프로젝트 이름
    category: "카테고리",             // Game, Creative, Utility, Portfolio, Mobile 등
    description: "프로젝트 설명",     // 설명 문구
    url: "https://프로젝트주소",      // 실제 Vercel 프로젝트 URL
    icon: "아이콘이름",               // Lucide 아이콘 이름
    status: "live",                   // "live" (초록) 또는 "progress" (노랑)
    tags: ["기술1", "기술2"]          // 사용한 기술 스택
}
```

---

## 📝 실전 예시

### 예시 1: 새 프로젝트 추가하기

배열 안에 새 항목을 추가하세요:

```javascript
const projects = [
    // 기존 프로젝트들...
    {
        title: "날씨 앱",
        category: "Utility",
        description: "실시간 날씨 정보를 제공하는 웹 애플리케이션입니다.",
        url: "https://my-weather-app.vercel.app",
        icon: "cloud-rain",
        status: "live",
        tags: ["React", "API", "TailwindCSS"]
    }
];
```

### 예시 2: 프로젝트 URL 변경하기

```javascript
{
    title: "게임 프로젝트 1",
    url: "https://my-awesome-game.vercel.app",  // ← 여기만 변경!
    // ... 나머지는 그대로
}
```

### 예시 3: 상태 변경하기

```javascript
{
    title: "모바일 앱",
    status: "live",  // "progress"에서 "live"로 변경!
    // ... 나머지는 그대로
}
```

### 예시 4: 프로젝트 삭제하기

해당 프로젝트 객체 전체를 삭제하세요:

```javascript
const projects = [
    {
        title: "게임 프로젝트 1",
        // ...
    },
    // 이 프로젝트를 삭제하려면 전체 { } 블록을 지우면 됨
    // {
    //     title: "삭제할 프로젝트",
    //     ...
    // },
    {
        title: "다른 프로젝트",
        // ...
    }
];
```

---

## 🎨 아이콘 변경하기

### 사용 가능한 아이콘 찾기
https://lucide.dev/icons/ 에서 원하는 아이콘 검색

### 추천 아이콘 목록

| 프로젝트 타입 | 아이콘 이름 |
|-------------|-----------|
| 게임 | `gamepad-2`, `joystick`, `trophy` |
| 웹사이트 | `globe`, `monitor`, `layout` |
| 모바일 앱 | `smartphone`, `tablet` |
| AI/ML | `brain`, `cpu`, `bot` |
| 데이터 | `database`, `bar-chart`, `pie-chart` |
| 디자인 | `palette`, `pen-tool`, `brush` |
| 코딩 | `code-2`, `terminal`, `file-code` |
| 유틸리티 | `lightbulb`, `tool`, `settings` |
| 쇼핑몰 | `shopping-cart`, `store` |
| 소셜 | `message-circle`, `users`, `heart` |

### 아이콘 변경 예시

```javascript
{
    title: "AI 챗봇",
    icon: "bot",  // gamepad-2에서 bot으로 변경
    // ...
}
```

---

## 🏷️ 카테고리 & 필터

### 기본 카테고리
- `Game` - 게임
- `Creative` - 크리에이티브
- `Utility` - 유틸리티
- `Portfolio` - 포트폴리오
- `Mobile` - 모바일

### 새 카테고리 추가하기

1. 프로젝트에 새 카테고리 이름 사용:
```javascript
{
    title: "AI 프로젝트",
    category: "AI",  // 새 카테고리!
    // ...
}
```

2. 필터 탭도 추가하려면 HTML 부분 수정:
```html
<div class="filter-tabs">
    <div class="filter-tab active">All Projects</div>
    <div class="filter-tab">Games</div>
    <div class="filter-tab">AI</div>  <!-- 새 탭 추가 -->
</div>
```

---

## 💡 자주 묻는 질문

### Q: 프로젝트 순서를 바꾸고 싶어요
A: 배열에서 프로젝트 순서를 바꾸면 됩니다!

### Q: 프로젝트가 10개 이상이에요
A: 상관없어요! 배열에 계속 추가하면 자동으로 그리드에 배치됩니다.

### Q: 필터 기능이 작동하나요?
A: 네! 자동으로 작동합니다. 필터 탭을 클릭하면 카테고리별로 필터링됩니다.

### Q: 실수로 문법 오류를 만들었어요
A: 쉼표(`,`)와 중괄호(`{ }`)를 확인하세요. JavaScript 문법 검사기를 사용하면 도움이 됩니다.

---

## 🚀 수정 후 배포

### GitHub에서 수정한 경우
1. 파일 하단 "Commit changes" 클릭
2. Vercel이 자동으로 재배포! (약 1분 소요)
3. 완료!

### 로컬에서 수정한 경우
```bash
git add index.html
git commit -m "프로젝트 정보 업데이트"
git push
```

---

## 🎯 핵심 포인트

✅ **한 곳만 수정**: `const projects = [...]` 배열만 수정하면 끝!
✅ **HTML 수정 불필요**: 프로젝트 카드는 자동 생성됨
✅ **필터 자동 작동**: 카테고리별 필터링 자동 지원
✅ **무한 확장 가능**: 프로젝트를 원하는 만큼 추가 가능

---

## 🔧 전체 템플릿

새 프로젝트를 추가할 때 이 템플릿을 복사해서 사용하세요:

```javascript
{
    title: "프로젝트 이름을 입력하세요",
    category: "Game",  // Game, Creative, Utility, Portfolio, Mobile 중 선택
    description: "프로젝트 설명을 입력하세요. 1-2문장 정도가 적당합니다.",
    url: "https://your-project.vercel.app",
    icon: "gamepad-2",  // lucide.dev에서 아이콘 선택
    status: "live",  // live 또는 progress
    tags: ["기술1", "기술2", "기술3"]
}
```

---

이제 프로젝트 관리가 정말 쉬워졌죠? 🎉
질문이 있으면 언제든 물어보세요!