---
title: SSH 키
owner: DevOps셀
status: 미확인
last_checked: 2026-11-17
sources:
  - https://app.notion.com/p/3561f5a71344800288cdcca98168f19a  # 비개발자를 위한 Bitbucket 사용 가이드, 2026-09-16 수정
  - https://backpackr-talk.slack.com/archives/C4UJHLN2X/p1793872519119169  # Bitbucket SSH 호스트 변경 공지
---

# SSH 키

## 먼저 물어볼 것

"SSH 키 발급"은 용도에 따라 답이 다르다. **무엇에 접속하려는지 먼저 확인한다.**

- Bitbucket에서 코드를 받거나 올리려는 것인가 → A
- 서버(EC2 등)에 접속하려는 것인가 → B

전사 표준 문서는 없다. 아래 A는 Notion 문서에서 확인된 내용이고, B는 확인된 절차가 없다.

## A. Bitbucket 접근

**SSH 키를 발급받을 필요가 없다.** 현행 공식 안내는 HTTPS와 브라우저 SSO다.

1. **계정 신청**: flex 워크플로우 `Bitbucket 사용신청/삭제 및 Repo 권한신청`
   - Flex 로그인 → 워크플로우 → 문서 작성하기 → 검색창에 `bit` 입력
   - 입력 항목: 신청 사유, 기타 요청(Admin 권한 등 일반적이지 않은 요청), Repo명, 권한(`write`)
2. **인증**: 개인 PC에서는 `git clone` 할 때 브라우저 SSO가 자동으로 진행된다(Git Credential Manager). 별도 토큰이나 키 발급이 필요 없다. 최초 1회 로그인 창에서 `Sign in with your browser`를 누른다.
3. **clone 주소**: Bitbucket 웹에서 저장소 → Clone → HTTPS 선택

참고
- 서버나 자동화에서는 API Token을 쓴다. **App Password는 폐지됐다.** 일부 셀 문서에 App Password 적용 방법이 남아 있지만 따르지 않는다.
- 그래도 SSH로 쓰려면 키는 회사가 발급하는 것이 아니라 본인이 만들어 Bitbucket 개인 설정의 SSH keys에 등록한다. 이 방식은 일부 셀 문서에만 있고 전사 표준이 아니다.
- 2026-11-12부터 Bitbucket SSH 호스트가 바뀐다는 전사 공지가 있었다. SSH를 쓰고 있다면 공지 원문을 확인한다.

문의: `#g_cell_devops`의 `@cloud-engineer`

## B. 서버 접속용 키

현행 절차 문서를 찾지 못했다. Notion에는 2020년 자료(Deprecated)만 있다.
추측해서 안내하지 말고 `#g_cell_devops`에 문의하도록 연결한다. 문의할 때 적을 내용: 접속하려는 서버나 서비스, 필요한 이유, 필요한 기간.

## 관련

- DB 접근 권한은 SSH 키가 아니라 Jira "DevOps셀" 프로젝트의 이슈로 신청한다. [workflows.md](../workflows.md) 참고.
- VPN 계정은 입사 시 사번 계정으로 발급된다. 사용법은 Notion `Forticlient VPN 사용법`.
