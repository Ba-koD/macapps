# Mac 사용 앱/설정 정리

자주 쓰는 앱과 터미널 도구, 입력기 관련 설정을 정리한 문서입니다.

## 1) 사용 중인 앱

### 시스템/입력/윈도우 관리
- **Scroll Reverser**: 터치패드/마우스 휠 스크롤 방향 반전
- **Karabiner-Elements**: 외부 키보드 키 매핑
- **AltTab**: macOS에서 Windows 스타일 `Alt+Tab` 전환
- **Rectangle**: 창 크기/위치 조절
- **Snap**: Windows의 `Win + 숫자키` 느낌으로 창 전환
- **구름입력기**: 한/영 입력기 사용 (입력 전환은 아래 추가 설정 참고)

### 배터리/리소스 모니터링
- **Battery Health 2**: 배터리 상태 상세 확인
- **AlDente**: 배터리 최대 충전 제한
- **RunCat**: 메뉴바에서 간단한 리소스 확인
- **Hot**: CPU 온도 확인
- **Memory Diag**: 메모리 관리 앱 (상황에 따라 누수 체감 있음)

### 생산성/기타
- **Maccy**: 클립보드 저장 (`App Store`는 유료, `brew` 설치 시 무료)
- **Amphetamine**: 잠자기 방지 (현재는 사용 빈도 낮음)
- **iStudiez Pro**: 시간표/과제/시험 일정 관리 (초기 설정량 다소 많음)
- **MenubarX**: 메뉴바 앱 정리 용도 (현재 유료 전환)
- **Ice**: MenubarX 대체 가능한 무료 앱
- **Alacritty**: 빠른 터미널 (`iTerm`보다 빠르고 단순)

## 2) 유용한 터미널 프로그램
- **Homebrew (`brew`)**: 필수 패키지 관리자 (`apt`와 유사)
- **zsh**: 기본 `bash`의 불편한 부분 보완, 테마/플러그인 풍부
- **btop**: 리소스 사용량을 시각적으로 보기 쉬움
- **Atuin**: 터미널 명령어 히스토리 검색/재사용 편리
- **Starship**: 여러 쉘(`zsh`, `bash`, `fish` 등)에서 공통으로 쓰는 빠른 프롬프트 커스터마이저

## 3) 기타 설정 및 프로그램
- **Arc**: 디자인이 깔끔하고 다중 구글 계정 관리에 편리(개발 중단, 보안 패치만 진행)
- **Zen Browser**: Firefox 계열을 선호하면 대안으로 사용 가능
- **powerlevel10k**: `zsh` 프롬프트 테마(Starship으로 대체)
- **MesloLGS NF**: Nerd Font 아이콘 지원 폰트

## 4) 추가 정보: 구름입력기 + 오른쪽 Command 키

구름입력기 사용 시, `right_command` 키로 한/영 변환하면 반응성이 더 좋을 때가 있습니다.
다만 `right_command + Q/W/R` 조합이 시스템 단축키로 같이 동작하는 문제가 있어, Karabiner-Elements에 아래 Complex Modification을 추가해 충돌을 막을 수 있습니다.

```json
{
  "description": "Disable all right Command key combinations",
  "manipulators": [
    {
      "from": {
        "any": "key_code",
        "modifiers": { "mandatory": ["right_command"] }
      },
      "to": [{ "key_code": "right_command" }],
      "type": "basic"
    }
  ]
}
```
