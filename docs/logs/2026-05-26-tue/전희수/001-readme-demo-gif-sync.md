# 작업 로그

## 날짜

2026-05-26

## 작성자

전희수

## 관련 브랜치 / PR

- 브랜치: develop
- PR: 미정

## 작업 목적

- GitLab 저장소에만 있던 README 기능 데모 섹션과 데모 GIF 자산을 GitHub 공개 저장소에 반영한다.

## 변경 요약

- GitLab `develop`의 README 기능 데모 섹션을 GitHub `develop`에 반영했다.
- `docs/image/demo/` 아래 데모 GIF 18개와 빈 폴더 보존용 `.gitkeep`를 추가했다.
- GitLab README가 참조하던 `docs/image/demo/04-ai-chat.gif`는 GitLab 모든 브랜치에도 실제 파일이 없어, 존재하는 `docs/image/demo/workboard/입력.gif`로 교체했다.

## 주요 파일

- `README.md`
- `docs/image/demo/`
- `docs/image/demo/workboard/`

## 테스트 / 확인

- GitHub `develop`과 GitLab `develop`의 미디어 파일 목록을 비교해 GitHub에 없는 GIF 18개를 확인했다.
- README에서 참조하는 로컬 미디어 경로 31개가 모두 실제 파일로 존재하는지 스크립트로 확인했다.

## 결정 / 이슈

- `04-ai-chat.gif`는 GitLab 원본 README에만 참조가 있고 파일은 존재하지 않아 그대로 옮기면 GitHub README에서 깨진 이미지가 된다.
- 깨진 참조를 피하기 위해 기능 데모 표의 해당 칸을 `workboard/입력.gif` 기반의 "작업 입력" 데모로 조정했다.

## 다음 단계

- 실제 AI 채팅 데모 GIF가 준비되면 `docs/image/demo/04-ai-chat.gif`로 추가하고 README의 "작업 입력" 칸을 교체한다.
