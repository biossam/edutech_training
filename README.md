# AI·에듀테크 연수

교원 연수 강의 사이트입니다(강사 장혜림). 성장 MAP(snja_map) 사이트와 같은 틀로 만들었습니다.

- 강사 화면: https://biossam.github.io/edutech_training/
- 참여자용 화면: https://biossam.github.io/edutech_training/?view=student (강의 PPT와 실습 링크만 보임, 첫 화면의 "참여자용 QR 코드 보기"로 띄우기)

## 강의 구성

| 강 | 제목 | PPT |
|---|---|---|
| 1 | 캔바로 디지털 학급 만들기 — 과제 할당부터 동영상 편집까지 | 34장 + 자동 자막 시연 영상 |
| 2 | POE 챗봇으로 수업 설계하기 — 챗봇과 함께하는 초등 역사, 수학 수업 | 22장 |

강의 화면에는 PPT(발표자 메모 포함), 수업 모드(전체 화면 발표), 실습 순서, 생각해 볼 질문, 실습 바로 가기, 강의 PPT 내려받기(강사 화면만)가 있습니다.

## 강의 PPT 바꾸기

- 원본 PPT: `files/강번호/ppt.pptx`, 화면에 보이는 슬라이드 그림: `assets/slides/강번호/1.jpg …` (1280×720)
- PPT를 고치면 PowerPoint에서 "내보내기 → 파일 형식 변경 → JPEG"로 슬라이드 그림을 다시 만들어 넣고(파일 이름은 1.jpg, 2.jpg …), `data/course.json`의 `slides`(장 수·제목·발표자 메모)도 맞춰 주세요.

## 구조

```
index.html              화면 틀
assets/css/style.css    디자인
assets/js/app.js        동작 (강 목록, 강의 화면, 수업 모드, QR)
data/site.json          사이트 이름
data/course.json        ★ 강의·슬라이드·실습 링크
files/                  강의 PPT, 시연 영상
```

빌드 과정이 없는 정적 사이트이며 GitHub Pages로 무료 운영합니다. 내 컴퓨터에서 볼 때는 폴더에서 `python -m http.server 8000` 후 http://localhost:8000 에 접속하세요.
