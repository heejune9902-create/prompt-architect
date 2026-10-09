# Prompt Architect

맡기고 싶은 작업을 말하면, 그 작업에 맞는 **프롬프트와 지침 파일을 설계**해 주는 Claude 스킬입니다.

AI 에이전트 활용에 관한 최근 연구·발표에서 뽑은 16개 방법 모듈(검증 루프, 코드 계산, 컨텍스트 관리, 정답 대조, 최소 권한, 감시자 분리, 고정 분류 등)을 담고 있습니다. 작업을 진단한 뒤 **필요한 방법만 골라 조합**합니다. 모든 기법을 다 붙이지 않는 것이 핵심입니다.

## 무엇을 해 주나

- 작업 진단: 유형, 위험, 검증 가능성 (질문은 최대 3개)
- 방법 선택 표: 고른 방법과 뺀 방법, 각각의 이유
- 바로 붙여 넣어 쓰는 실행 프롬프트
- 필요하면 지침 파일 (`CLAUDE.md`, `AGENTS.md`, `SKILL.md` 형식)
- 프롬프트 시험 계획과 검토 에이전트 구성
- 승인하면 하위 에이전트로 프롬프트 시험(반복 실행과 채점)을 진행하고 채점표 보고

## 폴더 구성

| 경로 | 용도 |
| --- | --- |
| `skills/prompt-architect/SKILL.md` | Claude 스킬 본체 |
| `guide/prompt-architect-guide.md` | 스킬을 쓸 수 없는 AI(ChatGPT, Codex 등)에 첨부해 쓰는 지침 버전 |

## 설치

### Claude Code

```bash
git clone https://github.com/<your-id>/prompt-architect.git
mkdir -p ~/.claude/skills
cp -r prompt-architect/skills/prompt-architect ~/.claude/skills/
```

프로젝트에만 쓰려면 `~/.claude/skills/` 대신 프로젝트의 `.claude/skills/`에 넣습니다.

### claude.ai

`skills/prompt-architect` 폴더를 zip으로 묶어 설정의 스킬 메뉴에서 업로드합니다.

### 다른 AI 도구

`guide/prompt-architect-guide.md`를 대화에 첨부하고 아래처럼 요청합니다.

## 사용 예

```text
아래 태스크의 프롬프트와 지침 파일을 설계해줘.
사용할 곳: 채팅
태스크: 최근 3일 동안 SNS 숏폼에서 바이럴된 영상을 분석하고 싶어
```

Claude Code에서는 `/prompt-architect` 뒤에 태스크를 적어 바로 부를 수 있습니다.

## 주의

- 모듈의 근거는 대부분 동료심사 전 프리프린트나 기업 발표입니다. 효과를 보장하지 않으며, 설계한 프롬프트는 시험으로 확인해야 합니다.
- 프롬프트 시험은 반복 실행이라 사용량이 듭니다. 시험 전에 한 번 승인을 받습니다.
- 문서는 한국어로 작성되어 있습니다.

## 라이선스

MIT
