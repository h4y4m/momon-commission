# Mo Mon — Live2D Rigging Commission

Mo Mon의 Live2D 리깅 커미션 소개 및 포트폴리오 페이지입니다. 아트머그 게시글에 임베딩할 수 있도록 제작된 반응형 정적 웹사이트입니다.

**[홈페이지 바로가기](https://h4y4m.github.io/momon-commission/)**

## 주요 기능

- Premium / Standard / Basic / SD 타입별 쇼케이스 영상 9개
- 영상 캐러셀, 썸네일 선택, 모바일 스와이프 및 키보드 탐색
- 리깅 디테일 GIF 9개 슬롯 및 확대 팝업
- 리깅 타입별 가격과 추가 옵션 안내
- 협업 일러스트 작가 11명 소개 및 아트머그 링크
- 누적 리깅 작업 건수 및 기준 날짜 표시
- 커미션 공지사항
- PC, 태블릿, 모바일 대응

## 기술 구성

HTML, CSS, Vanilla JavaScript · GitHub Pages

별도의 빌드 과정이나 서버가 필요하지 않습니다. YouTube 영상 재생에는 인터넷 연결이 필요합니다.

## 파일 구조

```text
momon-commission/
├── index.html
├── README.md
└── assets/
    ├── face-x.gif
    ├── face-y.gif
    ├── face-diagonal.gif
    ├── body-x.gif
    ├── body-y.gif
    ├── body-diagonal.gif
    ├── interaction.gif
    ├── hair-physics.gif
    ├── accessory-3d.gif
    └── partner-{작가 UID}.jpg
```

위 구조는 코드에서 참조하는 파일 경로입니다. GIF 및 이미지가 누락되면 대체 표시가 나타납니다. 협업 작가 썸네일은 4:3 비율로 표시됩니다.

## 콘텐츠 수정

`index.html`에서 다음 항목을 관리합니다.

| 항목 | 수정 위치 |
| --- | --- |
| 쇼케이스 영상 및 기본 가격 | `plans` |
| 리깅 디테일 | `samples` |
| 추가 옵션 | `extras` |
| 협업 작가 및 할인 혜택 | `partners` |
| 누적 작업 건수 및 기준 날짜 | `.completed-stat` |
| 예약 상태 | `.status` |
| 공지사항 | `#notice` |

누적 작업 건수는 실제 완료 실적에 맞춰 수동 갱신합니다.

## 배포

GitHub 저장소의 Settings → Pages에서 Deploy from a branch, main, /(root)를 선택합니다. 이후 main 브랜치에 변경 사항을 커밋하면 GitHub Pages에서 다시 배포됩니다.

## 아트머그 임베딩

HTML 편집기에 다음 코드를 삽입합니다.

```html
<iframe
  src="https://h4y4m.github.io/momon-commission/"
  width="100%"
  height="4000"
  style="display:block;width:100%;border:0;margin:0;padding:0;"
  allow="autoplay; encrypted-media; fullscreen; picture-in-picture"
  allowfullscreen>
</iframe>
```

게시글 환경과 콘텐츠 길이에 따라 iframe 높이를 조절합니다. 아트머그의 iframe 허용 여부에 따라 표시가 제한될 수 있습니다.
