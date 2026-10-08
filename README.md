[README.md](https://github.com/user-attachments/files/33210913/README.md)
# FPS 감도 변환기 (FPS Sensitivity Converter)

게임마다 다른 마우스 감도 계산 방식(yaw 값)을 **cm/360°** 기준으로 통일해서,
한 게임에서 쓰던 손 감각을 다른 게임에서도 그대로 유지할 수 있게 변환해주는 웹 도구입니다.

🔗 **데모 링크**: https://github.com/ehdbs86084769-bot/sens-converter.git

## 기능
- 20개 이상의 인기 FPS 게임 간 감도 변환 (CS2, Valorant, Apex, Overwatch 2, CoD, R6S, Fortnite, PUBG, Destiny 2, Halo Infinite, Rust, Tarkov, The Finals 등)
- 일반 감도 + 줌/ADS(스코프) 감도 변환 모드 지원
- DPI, eDPI, cm/360°, inch/360° 자동 계산
- 게임별 yaw 값 참고표 제공
- ⇄ 버튼으로 원본/대상 게임 즉시 교체

## 로컬에서 보기
그냥 `index.html` 파일을 브라우저로 열면 바로 동작합니다. 별도 서버나 빌드 과정이 필요 없습니다.

## GitHub Pages로 배포하는 방법
1. GitHub에서 새 저장소(Repository) 생성 (예: `sens-converter`)
2. 이 저장소에 `index.html` 파일을 업로드 (웹에서 "Add file → Upload files"로도 가능)
3. 저장소의 **Settings → Pages** 메뉴로 이동
4. **Branch**를 `main` (또는 `master`), 폴더는 `/ (root)`로 선택 후 **Save**
5. 1~2분 후 `https://[깃헙아이디].github.io/[저장소이름]/` 주소로 접속 가능

## 수정하기
`index.html` 안의 `GAMES` 배열(자바스크립트)에 게임을 추가/수정하면 됩니다.
```js
{name:"게임이름", yaw:0.022, note:"설명"}
```
yaw 값이 작을수록 같은 마우스 이동량 대비 화면이 덜 돌아갑니다.

## 참고
yaw 값은 커뮤니티에서 검증된 값 기준이며, 게임 패치로 바뀔 수 있어 참고용입니다.
