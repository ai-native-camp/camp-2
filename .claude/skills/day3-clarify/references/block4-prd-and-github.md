# Block 4: PRD 작성 & GitHub 첫 제출

## EXPLAIN

### 1. PRD란?

PRD(Product Requirements Document)는 "이 프로젝트가 뭘 해결하고, 뭘 만드는지" 정리한 문서입니다.

**비유: 건축 설계도**

집을 짓기 전에 설계도를 그리듯, 프로젝트를 시작하기 전에 PRD를 씁니다. "누구의, 어떤 불편을, 어떻게 해결하는가"를 한 장에 정리하는 것입니다.

### 2. 왜 지금 PRD를 쓰나?

Day 1~3에서 배운 것들을 정리할 때입니다:
- Day 1: Claude Code 핵심 기능 7개를 배웠다
- Day 2: MCP를 연결하고 Context Sync 스킬을 만들었다
- Day 3: Clarify로 모호한 요구사항을 명확하게 만들었다

**지금이 가장 좋은 타이밍입니다.** 배운 기술을 기반으로 "나는 이걸 만들겠다"를 선언하는 문서가 PRD입니다.

### 3. PRD 템플릿

```markdown
# [프로젝트 제목]

## 문제
> 한 줄: 누구의, 어떤 불편을, 어떻게 해결하는가

- **현재 상태**: (구체적 수치 — 몇 건, 몇 분, 몇 명)
- **원하는 상태**: (1주 후 돌아가고 있을 모습)
- **성공 기준**: (숫자로 판단 가능한 것 1~2개)

## 스킬
| # | 스킬명 | 한 줄 설명 | 상태 |
|---|--------|-----------|------|
| 1 | `/my-skill-1` | 입력 → 출력 | ✅ 동작 / 🔨 진행중 |
| 2 | `/my-skill-2` | 입력 → 출력 | ✅ 동작 / 🔨 진행중 |

## 변화 기록
- **Day 1**: "처음 정의" →
- **Day 3**: "지금 정의" →
- **가장 크게 달라진 점**:
```

### 4. GitHub으로 제출하기

GitHub은 코드와 문서를 함께 관리하고 공유하는 온라인 서비스입니다. Google Docs의 코드 버전이라고 생각하세요.

**여러분의 개인 저장소(repo)가 이미 만들어져 있습니다.**

운영진이 캠프 시작 전에 여러분 각자의 GitHub ID로 private repo를 만들어뒀습니다:

```
https://github.com/ai-native-camp/{여러분의-github-id}
```

이 repo는 PRD만 넣는 곳이 아닙니다. 캠프 기간 동안 만드는 **모든 작업물**(스킬, PRD, 과제 결과물)이 여기에 쌓입니다. 캠프가 끝나면 여러분의 포트폴리오가 됩니다.

> **GitHub이 처음이라면?** [git-for-everyone](https://github.com/ai-native-camp/git-for-everyone) 플러그인을 설치하세요.
> 이 플러그인은 **1기 개발자 캠퍼들이 비개발자를 위해 직접 만든** Claude Code 플러그인입니다.
>
> ```
> /plugin install git-onboarding
> ```
>
> 설치 후 `/git-onboarding-auto`를 실행하면, 환경 점검 → Git 설정 → 파일 생성 → 브랜치 → PR 생성까지 **한 번에 자동 처리**합니다. 이미 설정이 된 환경이면 필요한 단계만 건너뛰고 바로 진행됩니다. 막히면 `/git-onboarding-help`로 용어 설명과 FAQ를 볼 수 있습니다.

**제출 과정 요약:**

```
[개인 repo clone] → [PRD 작성] → [브랜치에서 저장] → [PR로 검토 요청]
```

| 단계 | 명령 | 비유 |
|------|------|------|
| 내 repo 가져오기 | `gh repo clone ai-native-camp/{id}` | "내 폴더를 컴퓨터에 받기" |
| 브랜치 생성 | `git checkout -b prd` | "사본으로 저장" |
| 파일 등록 | `git add PRD.md` | "제출할 파일 선택" |
| 저장 | `git commit -m "..."` | "Ctrl+S의 Git 버전" |
| 업로드 | `git push origin prd` | "온라인에 올리기" |
| 검토 요청 | `gh pr create ...` | "제출 버튼 누르기" |

> **걱정하지 마세요.** Claude가 모든 명령어를 자동으로 실행합니다. 여러분은 내용만 채우면 됩니다.

---

## EXECUTE

### Step 0: 환경 체크

Claude에게 아래를 입력하세요:

```
git이 설치되어 있는지, gh CLI가 인증되어 있는지 확인해줘.
```

> 문제가 있으면 Claude가 해결 방법을 안내합니다. 모두 통과하면 다음 단계로.
>
> GitHub이 처음이라면 [git-for-everyone](https://github.com/ai-native-camp/git-for-everyone) 플러그인을 설치하세요. 1기 개발자 캠퍼들이 만든 Git 자동 온보딩 도구입니다. `/git-onboarding-auto` 한 줄이면 설정부터 PR까지 자동으로 진행됩니다.

### Step 1: 내 repo 가져오기

```
내 GitHub 개인 repo를 clone해줘.
내 GitHub ID를 물어봐줘.
repo 주소는 ai-native-camp/{내 GitHub ID}야.
```

> Claude가 GitHub ID를 물어본 뒤 `gh repo clone ai-native-camp/{id}`로 여러분의 개인 repo를 가져옵니다.

### Step 2: PRD 작성

```
오늘까지 배운 내용을 바탕으로 PRD를 작성해줘.
PRD 템플릿을 써서, 내가 캠프에서 만든 스킬 기반으로.
.claude/skills/ 폴더에 어떤 스킬이 있는지 먼저 확인해줘.
```

> Claude가 여러분이 만든 스킬 목록을 보여준 다음, PRD 초안을 작성합니다.

### Step 3: PRD 검증

Claude가 아래 8개 항목을 자동으로 검증합니다:

| # | 항목 | 필수 |
|---|------|------|
| 1 | 프로젝트 제목 | 필수 |
| 2 | 문제 섹션 | 필수 |
| 3 | 현재 상태 (10자 이상) | 필수 |
| 4 | 원하는 상태 (10자 이상) | 필수 |
| 5 | 성공 기준 (10자 이상) | 필수 |
| 6 | 스킬 섹션 | 필수 |
| 7 | 스킬 2개 이상 | 필수 |
| 8 | 변화 기록 | 필수 |

### Step 4: GitHub PR 제출

검증 통과 후:

```
PRD를 내 GitHub repo에 제출해줘. PR까지 만들어줘.
```

> Claude가 개인 repo에서 브랜치 생성 → commit → push → PR 생성을 자동으로 처리합니다.
> 완료되면 PR URL이 출력됩니다. 이 URL을 과제 제출에 사용합니다.

---

## QUIZ

```json
AskUserQuestion({
  "questions": [
    {
      "question": "PRD에서 가장 중요한 섹션은?",
      "header": "Quiz 4-1",
      "options": [
        {"label": "변화 기록", "description": "Day 1부터 지금까지의 변화 과정"},
        {"label": "문제 정의", "description": "누구의, 어떤 불편을, 어떻게 해결하는가"},
        {"label": "스킬 목록", "description": "만든 스킬의 이름과 상태"},
        {"label": "프로젝트 제목", "description": "한 줄로 요약한 프로젝트명"}
      ],
      "multiSelect": false
    },
    {
      "question": "GitHub에서 PR(Pull Request)이란?",
      "header": "Quiz 4-2",
      "options": [
        {"label": "코드를 삭제하는 요청", "description": "불필요한 코드를 정리"},
        {"label": "내 작업을 확인해주세요라는 검토 요청", "description": "운영진에게 보내는 제출 버튼"},
        {"label": "새 프로젝트를 만드는 명령", "description": "GitHub에 새 저장소 생성"},
        {"label": "다른 사람의 코드를 가져오는 것", "description": "외부 코드를 내 프로젝트에 복사"}
      ],
      "multiSelect": false
    }
  ]
})
```

**정답 4-1: 2번.** PRD의 핵심은 "문제 정의"다. 누구의, 어떤 불편을, 어떻게 해결하는가를 명확히 정의해야 나머지가 의미를 갖는다. 스킬 목록이나 변화 기록은 문제 정의를 뒷받침하는 보조 섹션이다.

**정답 4-2: 2번.** PR(Pull Request)은 "내 작업을 확인해주세요"라고 운영진에게 보내는 검토 요청이다. 제출 버튼을 누르는 것과 같다. 운영진이 확인 후 승인하면 반영된다.

### Day 3 과제

Slack **#day3** 채널에 아래를 공유하세요:

1. **Before/After**: Clarify 전후 요구사항 비교 (Block 1에서 체험한 결과)
2. **가장 의외였던 질문**: Claude가 던진 질문 중 "이건 생각 못했다" 싶었던 것
3. **PRD PR 링크**: 방금 제출한 GitHub PR URL
