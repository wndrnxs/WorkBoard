# WorkBoard

검사기 프로젝트의 일정, 할 일, 자재 입고를 한 화면에서 관리하는 단일 파일 웹앱입니다.

## 주소

- 앱: https://workboard-3460b.web.app
- 로그인: Firebase Authentication(이메일·비밀번호). 계정은 Firebase 콘솔에서 직접 추가합니다.

## 구성

| 파일 | 내용 |
|---|---|
| `index.html` | 앱 전체(HTML·CSS·JS 한 파일) |
| `firestore.rules` | Firestore 보안 규칙 |
| `firebase.json`, `.firebaserc` | Firebase Hosting 설정 |
| `.github/workflows/firebase-hosting.yml` | main에 합치면 자동 배포 |
| `docs/index.html` | 예전 GitHub Pages 주소를 앱으로 넘기는 안내 페이지 |

## 배포

`main` 브랜치에 변경이 올라가면 GitHub Actions가 Firebase Hosting으로 자동 배포합니다.
저장소 시크릿 `FIREBASE_SERVICE_ACCOUNT` 에 Firebase 서비스 계정 키(JSON)가 필요합니다.

## 보안 규칙 적용

`firestore.rules` 의 내용을 Firebase 콘솔 → Firestore Database → 규칙 에 붙여 넣고 게시합니다.
