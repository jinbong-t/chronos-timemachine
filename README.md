# 고장 난 타임머신: 마지막 카운트다운

중1 '기술의 세계' 4인 1조 방탈출 수업용 웹앱(크로노스 콘솔)입니다.

| 주소 끝 | 화면 |
| --- | --- |
| `#t1` ~ `#t8` | 모둠별 학생 화면 (탑승권 QR) |
| `#teacher` | 교사 콘솔 (시동 화면 · 대시보드 · 설정) |

## 파일 구성

- `index.html` : 앱을 불러오는 로더
- `app/app1.txt` ~ `app6.txt` : 웹앱 본문(한 파일을 여섯 조각으로 나눔)
- `media/` : 영상 파일(v1_opening.mp4, v2_warp_past.mp4, v3_hall_panel.mp4, v4_door_open.mp4)을 여기에 올리면 자동 재생됩니다. 없으면 기본 효과로 대체됩니다.
- `firestore.rules` : Firebase로 실시간 연동할 때 쓰는 보안 규칙

## 실시간 연동

`app/app2.txt`의 `const FIREBASE_CONFIG = null;`을 Firebase 웹앱 설정 객체로 바꾸면 모든 태블릿과 교사 화면이 실시간으로 연동됩니다. null이면 데모 모드(한 기기 안에서만 연동)입니다.
