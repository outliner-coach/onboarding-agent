# 서비스 공식 문서

기준일: 2026-11-17. 회사에서 쓰는 외부 서비스의 공식 도움말 중, 사내 가이드와 맞닿는 문서를 모았다.

## 언제 쓰나

사내 지식과 공식 문서는 답하는 질문이 다르다.

| 질문 | 근거 |
| --- | --- |
| 누구에게, 어디에 신청하나. 회사 규칙이 무엇인가 | 사내 가이드 (`guides/`, `workflows.md`) |
| 그 서비스 화면에서 어떻게 하나. 기능이 어떻게 동작하나 | 이 파일의 공식 문서 |

- 제품 조작법을 물으면 공식 문서 링크를 준다. 메뉴 이름과 화면은 제품이 바뀌면 달라지므로, 사내 문서에 옮겨 적은 조작법보다 공식 문서가 정확하다.
- **회사 설정이 공식 문서보다 우선한다.** 공식 문서에 "할 수 있다"고 나와도 회사 관리자가 막아 둔 기능이 있다(외부인 초대, 그룹 생성, 게스트 초대 등). 사내 가이드에 창구가 정해져 있으면 그 창구로 안내하고, 공식 문서는 배경 설명으로만 쓴다.
- 이 표에 없는 서비스나 문서가 필요하면 그 서비스의 공식 도움말 도메인에서만 찾는다. 블로그나 커뮤니티 글을 근거로 쓰지 않는다.
- 답변에는 사내 근거와 공식 문서를 구분해서 적는다.

## Google Workspace

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 비밀번호 변경·재설정 | [비밀번호 변경 또는 재설정](https://support.google.com/mail/answer/41078) | 분실했거나 잠겼으면 프렌즈셀에 초기화 요청 ([guides/accounts-and-access.md](guides/accounts-and-access.md)) |
| Gmail 서명 만들기 | [Gmail 서명 만들기](https://support.google.com/mail/answer/8395) | 회사 서명 형식은 Notion `메일 서명 설정하기`(https://app.notion.com/p/5d6824ea27f546019c33a6f2646ab76c) |
| 그룹(그룹메일) 만들기와 설정 | [그룹 만들기 및 그룹 설정 선택](https://support.google.com/groups/answer/2464926) | 구성원 추가와 권한 변경은 프렌즈셀에 요청. 직접 만들 수 있는지는 확인 필요 |
| 공유 드라이브 역할의 차이 | [공유 드라이브에서 파일 액세스가 작동하는 방식](https://support.google.com/a/users/answer/12380484) | 권한 부여는 프렌즈셀에 요청 |
| 공유 드라이브에 파일 저장·공유 | [공유 드라이브로 파일 또는 폴더 저장 및 공유](https://support.google.com/drive/answer/7286514) | |
| 파일·폴더 공유와 액세스 관리 | [Google Drive 파일 및 폴더 공유](https://support.google.com/drive/answer/7166529) | |
| 캘린더 일정에 회의실 추가 | [일정에 회의실 추가](https://support.google.com/calendar/answer/143753) | 회의실 규칙은 [guides/meeting-rooms.md](guides/meeting-rooms.md) |

공유 드라이브 역할은 다섯 가지다: 관리자, 콘텐츠 관리자, 참여자, 댓글 작성자, 뷰어. 참여자는 파일을 수정하고 올릴 수 있지만 옮기거나 지울 수 없다. 옮기거나 지워야 하면 콘텐츠 관리자가 필요하다.

## Slack

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 다른 회사 사람을 채널에 초대 (Slack Connect) | [Slack Connect로 다른 회사와 채널에서 협업](https://slack.com/help/articles/360035092414-Use-Slack-Connect-to-work-with-other-companies-in-channels) | `#_qna_genie`에 채널 이름과 이메일을 올려 프렌즈셀에 요청 |
| 유저그룹 만들기·수정 | [유저그룹 만들기 및 편집](https://slack.com/help/articles/212906697-Create-and-edit-user-groups) | 프렌즈셀에 요청 |
| 표시 이름 바꾸기 | [표시 이름 변경](https://slack.com/help/articles/216360827-Change-your-display-name) | 회사 표기 규칙은 Notion `노션/슬랙 대화명 변경`(https://app.notion.com/p/854e28ced0d54237b8125d16b7b265d1) |
| 프로필 편집 | [프로필 편집](https://slack.com/help/articles/204092246-Edit-your-profile) | |

Slack Connect에 대해 공식 문서가 알려 주는 것
- 관리자가 외부인 초대 권한을 제한할 수 있다. 메뉴가 보이지 않으면 관리자에게 요청해야 한다.
- 초대장은 14일 뒤 만료된다. 만료되면 다시 보내야 한다.
- 초대받는 회사도 Slack 유료 요금제를 써야 한다.
- 상대 회사 설정에 따라 그쪽 관리자의 승인이 필요할 수 있다.
- `#general` 채널에는 외부인을 초대할 수 없다.

## Notion

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 페이지 공유와 권한 수준 | [공유 및 권한 설정](https://www.notion.com/help/sharing-and-permissions) | |
| 멤버·게스트 추가 | [멤버, 관리자, 게스트 관리](https://www.notion.com/help/add-members-admins-guests-and-groups) | 게스트 초대 창구는 확인하지 못했다 |

게스트는 페이지 단위로만 초대된다. 회사 도메인 이메일로 초대하면 게스트가 아니라 멤버로 추가된다.

## Atlassian (Jira, Confluence, Bitbucket)

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 표시 이름(공개 이름) 바꾸기 | [프로필 및 공개 범위 설정 업데이트](https://support.atlassian.com/atlassian-account/docs/update-your-profile-and-visibility-settings/) | 직접 바꿀 수 없으면 `#_qna_genie`에서 DevOps셀에 요청 ([guides/jira.md](guides/jira.md)) |
| Bitbucket SSH 키 설정 (macOS) | [macOS에서 개인 SSH 키 설정](https://support.atlassian.com/bitbucket-cloud/docs/set-up-personal-ssh-keys-on-macos/) | 회사 표준은 SSH가 아니라 HTTPS와 브라우저 SSO ([guides/ssh-key.md](guides/ssh-key.md)) |
| Bitbucket SSH 키 설정 (Windows) | [Windows에서 개인 SSH 키 설정](https://support.atlassian.com/bitbucket-cloud/docs/set-up-personal-ssh-keys-on-windows/) | 위와 같음 |
| App Password 폐지 일정 | [Bitbucket Cloud의 API 토큰 전환 안내](https://www.atlassian.com/blog/bitbucket/bitbucket-cloud-transitions-to-api-tokens-enhancing-security-with-app-password-deprecation) | |
| HTTPS 인증(Git Credential Manager) | [GCM의 Bitbucket 인증 문서](https://github.com/git-ecosystem/git-credential-manager/blob/main/docs/bitbucket-authentication.md) | |

App Password는 Atlassian이 2025년 6월에 폐지를 발표했고, 2025년 9월부터 새로 만들 수 없게 됐으며, 2026년 중반에 기존 것도 비활성화됐다. 사내 문서 중 App Password 적용 방법을 안내하는 것은 낡은 문서다.

## flex

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 사용 가이드 첫 화면 | [flex 사용 가이드](https://guide.flex.team/ko/) | Notion `flex 사용 가이드` |
| 휴가 등록과 내 휴가 관리 | [flex 웹에서 휴가 등록 및 내 휴가 관리](https://guide.flex.team/en/articles/10229315-registering-leave-and-managing-my-leave-on-flex-web) | 휴가 종류와 규칙은 [guides/leave-types.md](guides/leave-types.md) |
| 근무 등록과 조회 | [근무 등록 및 조회](https://guide.flex.team/en/articles/10294052-work-registration-and-viewing) | 회사 규칙은 [guides/attendance.md](guides/attendance.md) |
| 재직·경력증명서 내려받기 | [내 문서 업로드와 재직·경력증명서 다운로드](https://guide.flex.team/en/articles/10304345-uploading-to-my-documents-downloading-employment-career-certificates) | [guides/hr-documents.md](guides/hr-documents.md) |
| 연차 사용 계획 문서 작성 | [연차 사용 계획 문서 작성](https://guide.flex.team/en/articles/10288632-writing-an-annual-leave-usage-plan-document) | [guides/leave-request.md](guides/leave-request.md) |

- 연속된 날짜로 휴가를 등록할 때 반차 같은 세부 일정은 「세부 일정 수정」에서 따로 지정해야 한다. 그냥 등록하면 모든 날이 종일 휴가로 차감된다.
- 근무를 종료한 뒤 확인 버튼까지 눌러야 기록이 확정된다. 누르지 않으면 다음 날 출근 시각만 남는다.
- 2027년 1월 예정으로 friends-erp로 옮겨 가면 flex 공식 문서는 해당 없다. [guides/friends-erp.md](guides/friends-erp.md) 참고.

## Apple (macOS)

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| 비공개 Wi-Fi 주소 끄기 | [Mac에서 비공개 Wi-Fi 주소 사용하기](https://support.apple.com/guide/mac-help/use-a-private-wi-fi-address-on-mac-mchlb1cb3eb4/mac) | 사내 업무망 연결 전에 꺼야 한다 ([guides/wifi.md](guides/wifi.md)) |
| iPhone·iPad 포함 전체 설명 | [Apple 기기에서 비공개 Wi-Fi 주소 사용하기](https://support.apple.com/102509) | 모바일 테스트망을 쓸 때 참고 |

macOS 15 이상: 시스템 설정 → Wi-Fi → 네트워크 이름 옆의 세부사항 → 비공개 Wi-Fi 주소를 `끔`으로 바꾼다. 네트워크별 설정이라 사내 업무망에만 적용된다.

## Adobe

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| Creative Cloud 앱 설치 | [Creative Cloud 앱 다운로드 및 설치](https://helpx.adobe.com/download-install/apps/download-install-apps/creative-cloud-apps/download-creative-cloud-apps.html) | 라이선스는 결재 서식 `Adobe 계정 신청/삭제 요청`으로 먼저 받는다 |

## Fortinet (VPN)

| 할 일 | 공식 문서 | 사내에서는 |
| --- | --- | --- |
| FortiClient로 VPN 연결 | [SSL 또는 IPsec VPN 연결](https://docs.fortinet.com/document/forticlient/7.4.2/administration-guide/6364/connecting-to-ssl-or-ipsec-vpn) | 설치부터 로그인까지 [guides/vpn.md](guides/vpn.md). 설정값은 Notion `Forticlient VPN 사용법` |
| FortiClient VPN 내려받기 | [포티넷 제품 다운로드](https://www.fortinet.com/kr/support/product-downloads) | |

공식 문서는 설치된 FortiClient 버전에 맞는 것을 본다.

## 아직 공식 문서를 확인하지 않은 서비스

Figma, Microsoft 365, 산돌구름, 고위드(도움말 후보를 찾았으나 열어 보지 못함), 신도리코 복합기 드라이버, 카카오 T 비즈니스, Claude와 ChatGPT, Bitdefender, JetBrains, Redash. 필요할 때 공식 도움말 도메인에서 찾아 이 파일에 추가한다.

## 확인이 필요한 것

- 링크는 2026-11-17에 검색으로 존재를 확인했다. 각 문서를 끝까지 읽고 대조한 것은 아니다.
- 한국어 문서 제목은 옮겨 적은 것이라 실제 페이지 제목과 다를 수 있다. flex의 두 문서는 영문 페이지 주소다.
- 회사의 Slack, Google Workspace, Notion 관리자 설정이 공식 문서의 기본 동작과 어디가 다른지는 프렌즈셀 확인이 필요하다.
