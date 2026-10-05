# Shopzy Cafe24 확장 프로그램

Cafe24 개발자센터의 앱 설정을 자동으로 입력하고 Shopzy에 앱 정보를 등록하는 Chrome 확장 프로그램입니다.

확장은 개발자 앱과 OAuth 설정 입력을 돕는 선택 사항입니다. Shopzy의 디자인 수정은 SFTP 연결로도 이용할 수 있습니다. 아래 안내는 Cafe24 OAuth를 사용할 때의 설정 방법입니다.

[최신 확장 프로그램 ZIP 다운로드](https://github.com/first-fluke/shopzy-extension/releases/latest/download/shopzy-extension.zip)

## 설치

1. 위 링크에서 `shopzy-extension.zip`을 내려받아 압축을 풉니다. 압축을 푼 폴더는 계속 보관하세요.
2. Chrome 주소창에 `chrome://extensions`를 입력하고 **개발자 모드**를 켭니다.
3. **압축해제된 확장 프로그램을 로드**를 누르고 `manifest.json`이 바로 들어 있는 폴더를 선택합니다.
4. **Shopzy Cafe24 디자인 API 자동화**가 표시되고 오류가 없는지 확인합니다.
5. Chrome 툴바의 확장 프로그램 메뉴에서 Shopzy를 고정합니다. 아이콘을 눌러 **Shopzy · Cafe24 연결 준비** 팝업이 열리면 설치 완료입니다.

Chrome 웹 스토어 설치와 자동 업데이트는 지원하지 않습니다. ZIP에 포함된 `install.html` 또는 팝업의 **설치·업데이트·도움말**에서 자세한 안내를 볼 수 있습니다.

## 사용

1. [Shopzy](https://shopzy.firstfluke.com/ko/dashboard)에 로그인하고 **내 계정 → 연동 설정 → API 키**에서 키를 발급합니다. 팝업에 몰 아이디와 API 키를 입력하고 **설정 저장**을 누릅니다. `myshop.cafe24.com`이라면 `myshop`만 입력하세요.
2. [Cafe24 개발자센터](https://developers.cafe24.com/admin/apps/front/manage)에 로그인한 뒤 **① Cafe24 앱 설정**을 누릅니다. 페이지 이동 후 팝업을 다시 열어 완료 여부를 확인하세요.
3. 크리덴셜이 캡처되면 **② Shopzy로 전송**을 누릅니다.
4. **③ Shopzy에서 몰 연결**로 대시보드를 열고 몰을 추가하거나 기존 몰을 선택합니다. 해당 몰의 **운영 연결** 버튼을 누르고 Cafe24 접근 권한을 승인합니다.

앱 정보 전송과 몰 추가가 끝나도 OAuth 연결은 완료되지 않습니다. 몰의 운영 연결 버튼으로 권한 승인을 진행하세요.

## 업데이트

1. 최신 ZIP을 내려받아 압축을 풉니다.
2. 기존에 Chrome에 로드했던 폴더의 파일을 새 파일로 덮어씁니다. 같은 폴더를 유지하면 저장한 설정을 계속 사용할 수 있습니다.
3. `chrome://extensions`에서 Shopzy 카드의 **새로고침** 버튼을 누릅니다.
4. 이미 열려 있던 Cafe24 개발자센터 탭도 새로고침합니다.
5. 팝업 아래 버전 번호와 오류 없는 화면을 확인합니다.

확장 프로그램을 삭제하고 다시 설치할 필요는 없습니다.

## 문제 해결

- **manifest.json을 찾지 못함:** ZIP을 먼저 압축 해제하고 manifest.json이 바로 들어 있는 폴더를 선택하세요.
- **개발자센터에서 응답 없음:** 개발자센터 탭을 새로고침한 뒤 다시 실행하세요.
- **자동 실행 중 멈춤:** 팝업에서 자동 실행을 중지하고 개발자센터 페이지를 새로고침한 뒤 다시 시작하세요.
- **전송 실패:** 팝업의 오류를 확인하고 로그인한 Shopzy 계정과 API 키를 확인한 뒤 다시 전송하세요. 캡처한 크리덴셜은 유지됩니다.

API 키와 Client Secret은 다른 사람에게 보내지 마세요. 확장은 이를 Chrome 로컬 저장소에 보관하고 Shopzy로 전송할 때 HTTPS를 사용합니다.

[버전별 변경 내역](https://github.com/first-fluke/shopzy-extension/releases)
