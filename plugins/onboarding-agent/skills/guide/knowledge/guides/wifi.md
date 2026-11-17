---
title: 사내 와이파이 세팅
owner: DevOps셀
status: 문서확인
last_checked: 2026-11-17
sources:
  - https://app.notion.com/p/ee9db86c1ec34bdf9f592c9ebaacb3f4  # 사내 네트워크 이용하기(Wi-Fi), 2026-03-10 수정
  - https://backpackr-talk.slack.com/archives/C4UHULRPB/p1794376423038399?thread_ts=1794376410.220169&cid=C4UHULRPB
---

# 사내 와이파이 세팅

## 한 줄 요약

업무용 와이파이 `BPK_IAP`에 연결한 뒤, NAC 인증 포털에서 요구하는 설치와 인증 네 가지를 마쳐야 인터넷이 된다. 사용자 인증은 **매달 1일에 초기화**되므로 매달 다시 해야 한다.

## 망 종류

| SSID | 용도 | 조건 |
| --- | --- | --- |
| `BPK_IAP` | 업무용 인터넷망 | 아래 설치·인증 필요 |
| `BPK_TAP` | 모바일 테스트망(스테이지 접속) | 모바일 기기만. 목록에 보이지 않는 히든 방식 |
| `BPK_GAP` | 게스트용 | 신청 없이 인터넷만 사용. 사내 시스템(어드민, Redash, NAS 등)은 접근 불가 |

비밀번호는 여기에 적지 않는다. [Notion 원문](https://app.notion.com/p/ee9db86c1ec34bdf9f592c9ebaacb3f4)의 OS별 연결 방법에 있다.

## 절차 (`BPK_IAP`)

1. **와이파이 연결**
   - Windows: 화면 오른쪽 아래 Wi-Fi 아이콘 → `>` 버튼 → `BPK_IAP` → 연결 → 암호 입력
   - macOS: 화면 오른쪽 위 Wi-Fi 아이콘 → 다른 네트워크 → `BPK_IAP` → 암호 입력. 붙여넣기가 실패하면 직접 입력한다.
2. **(macOS 15 이상) 무작위 MAC 주소 끄기**: Wi-Fi 설정에서 '비공개 Wi-Fi 주소'를 끈다. 방법은 [무작위 MAC 주소 해제 가이드](https://app.notion.com/p/31f1f5a7134480bf91d5c56ab6249799).
3. **NAC 인증 포털 열기**: 처음 연결하면 인터넷이 안 되거나 특정 페이지로만 이동한다. 정상이다. 포털 주소는 Notion 원문의 "OS 공통" 항목에 있다.
4. **포털이 안내하는 대로 조치**
   - 백신 미설치 메시지 → Bitdefender 설치 (보통 지급 시 설치돼 있음)
   - NAC Agent 미설치 메시지 → 포털의 agent 페이지에서 OS에 맞는 agent 설치
   - 화면의 MAC 값에 취소선이 있음 → MAC 인증 페이지에서 자신의 MAC 주소를 입력해 인증
   - G-Suite 인증 메시지 → 페이지의 `인증` 버튼을 눌러 회사 구글 계정으로 인증
5. **매달 1일 이후 G-Suite 재인증**: 알림봇이 매월 1일 `#_qna_genie`에 공지한다.

MAC 주소 확인
- macOS: 애플 메뉴 → 이 Mac에 관하여 → 시스템 리포트 → 네트워크
- Windows: 명령 프롬프트에서 `ipconfig /all` → 어댑터별 물리적 주소

## 자주 막히는 곳

- 포털에서 인증서 경고가 뜬다 → 고급(advanced)을 눌러 계속 진행한다.
- 포털 새로고침이 안 된다 → 탭을 닫고 다시 연다.
- G-Suite 인증이 안 된다 → Safari 대신 Chrome으로 시도하고, 안 되면 재부팅한다.
- MAC 인증 후에도 안 된다 → 입력한 MAC 주소 오타를 확인한다.

## 그래도 안 되면

`#_qna_genie`에 증상을 올리고 DevOps셀 네트워크 담당을 찾는다. 올릴 내용: OS와 버전, 어느 단계에서 막혔는지, 포털에 표시된 메시지.

## 확인이 필요한 것

- Notion 문서 본문은 `BPK_IAP`, QnA는 `BPK_IAP_20F`로 SSID 표기가 다르다. 목록에 보이는 이름으로 연결한다.
- `BPK_TAP` 사용 신청은 예전 flex 전자결재 절차가 취소선 처리돼 있고 대체 절차가 없다. 모바일 외 기기 연결은 DevOps셀에 문의한다.
