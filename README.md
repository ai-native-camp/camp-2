# AI Native Camp - 2기

> 7일 후, 당신의 업무 방식은 영구적으로 바뀐다.

비개발자를 위한 Claude Code 7일 집중 캠프.

## Step 0: Claude Code 설치

스킬을 사용하려면 먼저 Claude Code가 설치되어 있어야 합니다.

### 사전 확인

| 항목 | 조건 |
|------|------|
| **OS** | macOS 10.15+, Ubuntu 20.04+/Debian 10+, Windows 10+ (WSL 필요) |
| **RAM** | 4GB 이상 |
| **네트워크** | 인터넷 연결 필수 (오프라인 사용 불가) |
| **셸** | Bash, Zsh, Fish |
| **계정** | Claude Pro, Max, Teams, Enterprise 중 하나 |

> **Node.js는 필요 없습니다.** 아래 방법(native installer)으로 설치하면 Node.js 없이 단독 실행됩니다.

### 설치 방법

터미널을 열고, 본인 OS에 맞는 명령어를 복사해서 붙여넣으세요.

**macOS / Linux / WSL:**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows (PowerShell):**

```powershell
irm https://claude.ai/install.ps1 | iex
```

**Windows (CMD):**

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

> 잘 모르겠으면 [https://claude.ai](https://claude.ai) 에 접속해서 "Claude Code 설치하는 방법 알려줘"라고 물어보세요. Claude가 단계별로 안내해줍니다.

### 설치 확인

터미널을 열고 아래 명령어를 입력합니다:

```
claude
```

Claude가 인사하면 성공입니다. 계정 인증(로그인) 안내가 나오면 그대로 진행하세요.

## Step 1: 스킬 설치

```bash
npx skills add ai-native-camp/camp-2 --agent claude-code --yes
```

이 한 줄이면 모든 커리큘럼 스킬이 Claude Code에 설치됩니다.

> 설치 후 Claude Code에서 `/day1-onboarding` 으로 시작하세요.

## Skills as Curriculum

이 캠프의 커리큘럼은 **Claude Code Skills 그 자체**다.

슬라이드를 넘기며 듣는 강의가 아니다. `/day1-onboarding`을 실행하면 Claude가 직접 가르치고, 질문하고, 실습을 안내한다. 매일 새로운 Skill이 열리고, 어제 배운 것 위에 오늘을 쌓는다.

Skill을 만드는 법을 Skill로 배운다. 이것이 이 캠프의 방식이다.

## 커리큘럼

| Day | Skill | 주제 |
|-----|-------|------|
| 1 | `day1-onboarding` | 7개 핵심 기능 (Memory, Skill, MCP, Subagent, Agent Teams, Hook, Plugin) |
| 2 | *coming soon* | |
| ... | | |

## 캠프가 끝나면

수료가 아니라 시작이다. Claude Code라는 불을 다루는 신인류 커뮤니티의 일원이 된다.
