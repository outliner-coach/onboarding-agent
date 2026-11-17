# onboarding-agent

백패커 구성원(배낭여행자)을 위한 사내 절차 안내 에이전트. Claude Code 플러그인으로 동작한다.

- **메인 타겟**: 재직자 — 어떤 일을 "처음" 해 보는 사람 (사내 와이파이 세팅, SSH 키, AI API 키 신청, Jira 발급, 택배 신청, 가족돌봄휴가 신청 등)
- **보조 타겟**: 신규 입사자
- **하는 일**: 문서에 근거한 절차 안내, flex 워크플로우 링크 제공, 담당 셀에 보낼 메시지 초안 작성

## 설치

이 레포는 private이다. 설치하는 사람의 git이 이 레포에 접근할 수 있어야 한다.

```bash
claude plugin marketplace add outliner-coach/onboarding-agent
```

```bash
claude plugin install onboarding-agent@backpackr-onboarding
```

설치 후 Claude Code에서 평소처럼 질문하거나 `/onboarding-agent:guide 와이파이 처음 연결하는 법`처럼 직접 부른다.

지금은 개인 레포에서 다듬는 단계다. 동료에게 배포할 때는 회사 Bitbucket의 사내 플러그인 마켓플레이스로 옮길 계획이다.

업데이트는 수동이다. 자동 업데이트는 `/plugin` → Marketplaces에서 켤 수 있다.

```bash
claude plugin marketplace update backpackr-onboarding
```

## 구조

```
.claude-plugin/marketplace.json          마켓플레이스 정의
plugins/onboarding-agent/
  .claude-plugin/plugin.json             플러그인 매니페스트
  skills/guide/
    SKILL.md                             답변 방식
    knowledge/
      index.md                           주제 색인
      guides/                            주제별 절차
      workflows.md                       flex 워크플로우 목록
      contacts.md                        담당 셀과 채널
      gaps.md                            알려진 공백과 상충
.claude/skills/update-knowledge/         지식 갱신용 스킬 (레포 관리자용)
research/                                최초 조사 기록
```

## 지식 갱신

지식의 정본은 이 레포의 `knowledge/` 폴더다. 원문은 Notion과 Slack `#_qna_genie`에 있다.

이 레포를 Claude Code로 열고 아래를 실행하면 가이드를 원문과 대조해 갱신한다. Notion과 Slack 커넥터가 필요하다.

```
/update-knowledge all
```

새 주제는 `/update-knowledge new <주제>`로 추가한다.

## 원칙

- 비밀번호, 공용 계정 정보, 계좌번호, 내부 IP와 내부 전용 주소, 개인 이름과 연락처는 이 레포에 기록하지 않는다. 필요한 곳에서는 Notion 원문 링크를 안내한다.
- 담당자는 셀과 채널로 적는다.
- 원문을 직접 확인하지 않은 내용에는 상태(`부분확인`, `미확인`)를 표시한다.

## 조사 기록

| 문서 | 내용 |
| --- | --- |
| [research/slack-qna-genie.md](research/slack-qna-genie.md) | Slack `#_qna_genie` 질문 유형과 해결 경로 (2026-09-03 ~ 11-17) |
| [research/notion-inventory.md](research/notion-inventory.md) | Notion "생활 백서" 문서 인벤토리와 공백 |
