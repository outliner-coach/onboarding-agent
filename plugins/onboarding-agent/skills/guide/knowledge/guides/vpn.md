---
title: VPN 연결
owner: DevOps셀
status: 문서확인
last_checked: 2026-11-17
sources:
  - https://app.notion.com/p/23f1f5a7134480dbbe7ef2beca934e1e  # Forticlient VPN 사용법, 2026-10-06 수정
  - https://app.notion.com/p/6233696b47354c5799705fe1d35b6c68  # AD 인증시스템 구축 및 내부시스템 계정연동, 2025-11-11 수정
  - https://backpackr-talk.slack.com/archives/C4UHULRPB/p1792464399781439?thread_ts=1792464388.037519&cid=C4UHULRPB  # 로그인 실패 시 조치
  - https://backpackr-talk.slack.com/archives/C4UHULRPB/p1793235860859759  # iPhone LTE에서 접속 불가
---

# VPN 연결

## 한 줄 요약

FortiClient VPN을 설치하고, Notion에 있는 설정 파일을 가져온 뒤 연결한다. PC는 회사 구글 계정으로, 휴대전화는 사번 계정(AD 계정)으로 로그인한다.

## 먼저 물어볼 것

어떤 기기인지 확인한다. PC(macOS, Windows)와 휴대전화(iPhone, Android)는 설정 방법과 로그인 계정이 다르다.

## 서버 주소와 설정값

서버 주소, 사전 공유 키 같은 설정값은 여기에 적지 않는다. [Notion `Forticlient VPN 사용법`](https://app.notion.com/p/23f1f5a7134480dbbe7ef2beca934e1e)에 있다. PC는 그 페이지의 설정 파일(`forticlient-vpn.conf`)을 내려받아 쓰므로 값을 직접 입력할 일이 없다.

## PC (macOS, Windows)

현행 방식은 **IPsec VPN + 설정 파일 가져오기**다. Notion 문서에서 SSL VPN 방식과 "직접 설정하기"는 취소선 처리돼 있다. 예전에 SSL VPN으로 설정해 둔 사람은 아래 방식으로 다시 설정한다.

1. **FortiClient VPN 설치**
   - Notion 문서 맨 위의 다운로드 링크를 쓴다. 링크가 안 되면 [포티넷 제품 다운로드](https://www.fortinet.com/kr/support/product-downloads) 페이지 맨 아래에서 FortiClient VPN을 받는다.
   - macOS: 설치 파일 실행 → FortiClientInstaller 실행 → 열기 → Install → 암호 입력 창이 나올 때까지 계속·동의·설치 → Mac 로그인 암호 입력. 설치가 끝나면 권한 요청을 허용하고, 시스템 설정에서 FortiTray를 허용한다.
   - Windows: 설치 파일 실행 → 약관 동의 → 설치.
2. **설정 파일 내려받기**: Notion 문서의 "설정 가져오기"에서 `forticlient-vpn.conf`를 내려받는다.
   - macOS는 파일을 `/Users/Shared` 폴더로 옮긴다. 다른 경로에 두면 디스크 접근 권한 오류로 실패한다.
3. **설정 가져오기**: FortiClient 실행 → 이용약관 동의 → 오른쪽 위 자물쇠 버튼으로 설정 잠금 해제 → 톱니바퀴 → 복구 → 설정 파일 선택 → 열기 → 확인.
4. **연결**: Connect를 누른다. 브라우저에 "안전하지 않음" 경고가 뜨면 고급을 눌러 계속 진행한다.
5. **로그인**: 회사 구글 계정으로 로그인한다. 연결되면 할당받은 IP와 구글 메일 주소가 표시된다.

FortiClient 화면 조작이 버전에 따라 다르면 [Fortinet 공식 문서](https://docs.fortinet.com/document/forticlient/7.4.2/administration-guide/6364/connecting-to-ssl-or-ipsec-vpn)에서 설치된 버전의 안내를 본다.

## 휴대전화 (iPhone, Android)

1. App Store 또는 Play 스토어에서 `FortiClient VPN`을 설치하고 권한 요청을 허용한다.
2. 연결 설정을 새로 추가한다(iPhone: Connection → Add Configuration). 유형은 IPsec VPN이다.
3. 설정값은 Notion 문서의 "iOS 설치 및 IPsecVPN 사용 방법" 또는 "Android 설치 및 IPSecVPN 사용 방법" 표를 그대로 입력한다. X-Auth를 켜고 사용자 이름에 **사번 계정**을 넣는다.
4. 연결을 켜고 사번 계정의 비밀번호를 입력한다. 비밀번호를 모르면 [ad-account.md](ad-account.md)를 본다.

## 자주 막히는 곳

| 증상 | 조치 |
| --- | --- |
| iPhone에서 LTE·5G로는 VPN 로그인이 안 된다 | iPhone은 이동통신망에서 IPv6로 통신을 시도해서 연결되지 않는다. Wi-Fi에 연결한 뒤 시도한다 |
| Mac을 iPhone 핫스팟에 연결했더니 구글 로그인 페이지가 열리지 않는다(`ERR_EMPTY_RESPONSE`, 시간 초과) | 통신사 회선이 IPv6 전용이면 생긴다. IPv6를 끈 네트워크 위치를 만들어 핫스팟을 쓸 때만 그 위치로 바꾼다. 터미널 명령과 순서는 Notion 문서의 "MACOS에서 iPhone 핫스팟으로 VPN 연결하기"에 있다 |
| 사번 계정으로 로그인이 실패한다 | 비밀번호 변경 페이지에서 비밀번호를 바꾼 뒤 다시 시도한다. 계정명을 대문자로 넣으면 실패하는 경우가 있다 |
| `too many` 메시지가 뜬다 | 짧은 시간에 로그인을 너무 많이 실패해 잠긴 것이다. 시간을 두고 다시 시도한다 |
| 집에서 접속이 안 된다 | 모바일 테더링으로 시도하거나 FortiClient를 다시 설치한다 |
| macOS에서 설정 파일을 가져올 때 권한 오류가 난다 | 설정 파일을 `/Users/Shared`로 옮겼는지 확인한다 |
| VPN은 연결됐는데 Bitbucket 같은 사내 서비스가 안 열린다 | FortiClient에 표시된 IP를 적어 `#_qna_genie`에 문의한다 |

## 그래도 안 되면

`#_qna_genie`에 올리고 DevOps셀 네트워크 담당을 찾는다. 올릴 내용: 기기와 OS 버전, 어떤 네트워크에서 시도했는지(집, 핫스팟, 사무실), 막힌 단계, 화면에 뜬 메시지.

## 확인이 필요한 것

- AD 계정 문서(2025-11)는 "VPN은 OS 공통으로 사번 계정 로그인"이라고 하고, VPN 문서(2026-10)의 PC 절차는 구글 계정 로그인이다. 더 최근 문서를 따라 PC는 구글 계정, 휴대전화는 사번 계정으로 적었다.
- Notion 문서의 화면 캡처는 읽지 못했다. 캡처에만 있는 단계가 빠졌을 수 있다.
- 사무실 안(사내망)에서 VPN을 연결할 수 있는지는 확인하지 못했다.
