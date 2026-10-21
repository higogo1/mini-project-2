# 타워디펜스 웹게임 (가제)

Phaser 3와 Vite로 만드는 브라우저 2D 타워디펜스 게임이다.
게임 이름은 아직 정하지 않았다. 정해지면 제목을 고친다.

저장소: https://github.com/higogo1/mini-project-2 (공개)

현재 단계: 기획 (코드 없음). 자세한 상태는 docs/progress.md를 본다.

## 처음 왔다면 읽는 순서

1. docs/progress.md: 지금 어디까지 했고 다음에 무엇을 할지
2. docs/tasks.md: 전체 작업 목록과 각 작업의 상태
3. docs/requirements.md: 무엇이 되어야 하나
4. docs/design.md: 어떤 구조로 만들까
5. AGENTS.md: 작업 규칙 (사람과 AI 도구 공통)

## 실행

구현 시작 후(작업 T-05 완료 후) 아래 명령이 동작한다.

```
npm install
npm run dev
```

브라우저에서 터미널에 표시된 주소(기본 http://localhost:5173)를 연다.

배포용 빌드:

```
npm run build
```

결과물은 dist 폴더에 생긴다.

## 필요 환경

- Node.js 20 이상
- npm

## 폴더 구조

상태: [있음] 이미 만든 파일, [예정] 작업 목록에 있지만 아직 없는 파일

```
mini project 2/
├─ README.md               [있음] 실행과 사용 방법, 읽는 순서
├─ AGENTS.md               [있음] 사람과 AI 도구가 지킬 작업 규칙
├─ package.json            [예정] 의존성과 실행 스크립트 (T-05)
├─ index.html              [예정] 게임을 담는 페이지 (T-05)
├─ src/
│  ├─ main.js              [예정] Phaser 게임 설정과 씬 등록 (T-06)
│  ├─ config.js            [예정] 화면 크기, 난이도 등 상수 (T-06)
│  ├─ scenes/
│  │  ├─ BootScene.js      [예정] 에셋 불러오기 (T-06)
│  │  ├─ MenuScene.js      [예정] 시작 화면 (T-08)
│  │  └─ GameScene.js      [예정] 실제 플레이 (T-06)
│  ├─ objects/             [예정] 플레이어, 적 같은 게임 오브젝트
│  └─ systems/             [예정] 점수, 저장 같은 공통 기능
├─ public/
│  └─ assets/              [예정] 이미지, 사운드 (출처는 assets/CREDITS.md에 기록)
└─ docs/
   ├─ requirements.md      [있음] 무엇이 되어야 하나
   ├─ design.md            [있음] 어떤 구조로 만들까, 결정 기록
   ├─ tasks.md             [있음] 어떤 순서로 구현할까
   └─ progress.md          [있음] 지금 어디까지 했나, 인수인계 메모
```

파일을 새로 만들거나 지우면 이 표도 같이 고친다.

## 자료

- 게임 데이터(레벨, 적 수치 등)는 src/data/ 아래 JSON으로 둘 예정이다. 위치가 확정되면 design.md에 기록한다.
- 진행 저장은 브라우저 localStorage를 쓸 예정이다. 저장 키와 형식은 design.md에 적는다.
