# 지식 색인

질문이 들어오면 이 표에서 주제를 찾고, 해당 가이드 파일만 읽는다.
표에 없는 주제는 [gaps.md](gaps.md)에서 알려진 공백인지 확인한다.

상태 값
- `문서확인`: Notion 원문에서 절차를 직접 확인함
- `부분확인`: 일부만 원문에서 확인됨. 빈 부분은 가이드 안에 표시
- `미확인`: 전사 표준 문서가 없음. 담당 셀 확인이 필요

| 주제 | 이런 질문에 | 가이드 | 담당 | 상태 | 기준일 |
| --- | --- | --- | --- | --- | --- |
| 계정·권한 신청 창구 | 권한 신청, 계정 신청, 어디에 신청, 어도비·포토샵, MS Office, 피그마, 폰트, Redash, 펜타곤·하노이, AWS, 슬랙 채널 초대, 외부인 초대, 그룹메일, 구글 드라이브 폴더 권한, 비밀번호 초기화, 공용 계정, DB 권한, 아르바이트 계정, 권한 삭제 | [guides/accounts-and-access.md](guides/accounts-and-access.md) | 프렌즈셀, DevOps셀 | 부분확인 | 2026-11-17 |
| 사내 와이파이 세팅 | 와이파이, wifi, BPK_IAP, NAC, nacpass, 인터넷 연결 안 됨, 인터넷 차단, 허용되지 않은 MAC 주소, 맥주소 등록, 장비 인증, 신규 입사자 맥북, 새 노트북 네트워크, 매달 인증, 게스트 와이파이 | [guides/wifi.md](guides/wifi.md) | DevOps셀 | 문서확인 | 2026-11-17 |
| VPN 연결 | VPN, FortiClient, 포티클라이언트, 재택 접속, 외부에서 사내 시스템 접속, VPN 로그인 실패, 핫스팟 VPN, 아이폰 VPN | [guides/vpn.md](guides/vpn.md) | DevOps셀 | 문서확인 | 2026-11-17 |
| AD 계정과 비밀번호 | AD 계정, 사번 계정, AD 비밀번호 초기화, 비밀번호 변경, VPN 비밀번호, NAS 로그인, b로 시작하는 계정 | [guides/ad-account.md](guides/ad-account.md) | DevOps셀 | 부분확인 | 2026-11-17 |
| SSH 키 | ssh 키 발급, ssh key, Bitbucket 인증, git clone 인증, 서버 접속 키, App Password | [guides/ssh-key.md](guides/ssh-key.md) | DevOps셀 | 미확인 | 2026-11-17 |
| AI API 키 | API 키 신청, OpenAI/Gemini/Claude API, AI 유료 툴, ChatGPT·Claude 구독 지원 | [guides/ai-api-key.md](guides/ai-api-key.md) | 프렌즈셀 | 문서확인 | 2026-11-17 |
| Jira·Confluence 계정 | 지라 발급, Jira 계정, Confluence, Atlassian 초대, 소프트웨어 계정 신청 | [guides/jira.md](guides/jira.md) | DevOps셀 | 부분확인 | 2026-11-17 |
| 택배·퀵·등기 | 택배 신청, 운송장, 송장 출력, 퀵 서비스, 등기, 우편물 | [guides/parcel.md](guides/parcel.md) | 프렌즈셀 | 문서확인 | 2026-11-17 |
| 가족돌봄휴가 | 가족돌봄휴가, 가족 간병, 부모님 병원, 돌봄 휴직 | [guides/family-care-leave.md](guides/family-care-leave.md) | 프렌즈셀(HR) | 부분확인 | 2026-11-17 |
| 휴가 종류와 규칙 | 휴가 종류, 경조 휴가, 병가, 공가, 예비군, 건강검진 반차, 배우자출산휴가, 난임, 휴가 증빙, 며칠 쓸 수 있나, 휴직, 무급 병가 | [guides/leave-types.md](guides/leave-types.md) | 프렌즈셀(HR) | 부분확인 | 2026-11-17 |
| friends-erp (flex 이관) | friends-erp, ERP, 새 인사시스템, flex 언제까지, 휴가·결재·출퇴근을 어디에 내야 하나, 에이전트 토큰 | [guides/friends-erp.md](guides/friends-erp.md) | 프렌즈셀 | 부분확인 | 2026-11-17 |

휴가, 근태, 결재 질문에는 [guides/friends-erp.md](guides/friends-erp.md)의 "지금 어디에 신청해야 하나"를 함께 확인한다. 2027년 초에 flex에서 friends-erp로 옮겨 갈 예정이다.

함께 쓰는 파일
- [workflows.md](workflows.md): 결재 서식(워크플로우) 97개 목록과 flex 직링크. "어디서 신청해?" 질문은 여기서 서식 이름을 먼저 찾는다
- [contacts.md](contacts.md): 영역별 담당 셀과 문의 채널
- [gaps.md](gaps.md): 아직 답이 없는 주제와 확인이 필요한 상충
- [official-docs.md](official-docs.md): Google, Slack, Notion, Atlassian, flex 등 서비스 공식 도움말. 제품 화면에서 어떻게 하는지는 여기서 찾는다
