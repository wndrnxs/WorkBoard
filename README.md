# WorkBoard

검사기 프로젝트의 일정, 할 일, 자재 입고를 한 화면에서 관리하는 단일 파일 웹앱입니다.

## 주소

https://wndrnxs.github.io/WorkBoard/

GitHub Pages(main 브랜치 루트)로 서비스되며, main에 변경이 올라가면 1~2분 안에 반영됩니다.

## 로그인과 저장

- 로그인: Firebase Authentication(이메일·비밀번호). 계정은 Firebase 콘솔 → Authentication → Users 에서 직접 추가합니다. 앱에 가입 화면은 없습니다.
- 저장: Firestore. 로그인한 계정끼리 같은 데이터를 보며, 기기가 달라도 동일하게 보입니다.
- Firebase에 연결하지 못하면 로그인 없이 열리고 그 브라우저에만 저장됩니다(임시 동작).

## 구성

| 파일 | 내용 |
|---|---|
| `index.html` | 앱 전체(HTML·CSS·JS 한 파일) |
| `firestore.rules` | Firestore 보안 규칙 |
| `manifest.webmanifest`, `icon-*.png` | 앱 설치용 정보와 아이콘 |

## 설정 체크리스트

1. Firestore → 규칙 탭에 `firestore.rules` 내용을 붙여 넣고 게시
2. Authentication → Settings → 승인된 도메인에 `wndrnxs.github.io` 추가
3. Authentication → Settings → User actions 에서 "Enable create (sign-up)" 해제(임의 가입 차단)
