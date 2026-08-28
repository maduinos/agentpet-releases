# AgentPet — Releases

AgentPet 배포 산출물(.deb) 저장소입니다.

AgentPet은 Codex, Claude Code, Cursor 에이전트 활동을 바탕화면 캐릭터로 보여 주고, 세션 행을 눌러 해당 터미널로 포커스를 돌려주는 Linux 데스크톱 앱입니다.

## 다운로드

최신 `.deb`는 [Releases](../../releases/latest) 에서 받을 수 있습니다.

## 설치 (Ubuntu 22.04 / 24.04 amd64)

```bash
sudo apt install ./agentpet_0.2.22_amd64.deb
```

Python이나 pip을 따로 설치할 필요는 없습니다. 런타임이 패키지에 포함되어 있습니다.

## 첫 실행

설치 후 애플리케이션 메뉴에서 **AgentPet**을 실행하거나, 터미널에서 `agentpet`을 실행합니다.

GUI 로그인 시 자동 시작을 쓰려면:

```bash
agentpet setup --autostart
```

## 지원 환경

- Ubuntu Desktop 22.04 / 24.04 LTS, amd64
- glibc 2.35 이상
- Linux 터미널 포커스 연동(Ghostty, GNOME 터미널 등)을 전제로 합니다

## 무결성 확인

릴리즈 노트의 SHA-256 값과 아래 명령 결과를 비교하세요.

```bash
sha256sum agentpet_0.2.22_amd64.deb
```

소스 코드와 개발 이슈는 [maduinos/AgentPet](https://github.com/maduinos/AgentPet) 저장소를 참고하세요.
