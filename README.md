# 노마드코더 플러터 웹툰 앱
## 6.0 ~ 6.3 정리
- dart http 라이브러리 적용
- 노마드코더에서 제공하는 웹툰 API로 오늘의 웹툰 JSON 데이터 불러오기
- JSON 데이터 파싱

## 6.4 ~ 6.6 정리
- 2개의 Build 방법
  1. StatefulWidget의 initState, setState를 이용한 빌드 (기본)
  2. StatelessWidget 상태에서 FutureBuilder를 이용한 빌드

## 6.7 정리
- ListView를 사용
- ListView는 3가지 방법으로 사용할 수 있다.
  1. ListView (비추천)
  2. ListView.builder 1개의 필수값이 존재함 (추천)
  3. ListView.separated 2개의 필수값이 존재함 (추천)
- builder와 separated를 추천하는 이유는 **사용자가 보고있는 화면의 값만 불러오고 보고있지 않은 화면은 메모리에서 삭제한다** 일반 ListView는 List에 담겨있는 모든 값을 불러온다.

## 6.8 정리
- ListView를 공통 메소드로 변경
- 웹툰 이미지 불러오기
  -. Image.network에 src(주소) 입력 및 User-agent 설정
     - 예시) https://image...
     - User-agent는 HTTP 요청을 보내는 디바이스와 브라우저 등 사용자 소프트웨어의 식별 정보를 담고 있는 request header의 한 종류이다. 임의로 수정될 수 없는 값이고, 보통 HTTP 요청 에러가 발생했을 때 요청을 보낸 사용자 환경을 알아보기 위해 사용한다.

## 6.9 정리
- widget 분리 및 상세페이지 화면 추가
- 목록화면(homeScreen)에서 웹툰 클릭 시 상세화면(detailScreen) 페이지로 이동
- GestureDetector 사용
  - 제스처를 감지하는 위젯(onTab 사용)
- Navigator.push 사용
  - 화면전환 할 때 사용
  - default 화면전환 애니메이션은 슬라이드 형식의 애니메이션이며, **fullscreenDialog: true**를 사용하면 화면전환 될 페이지가 아래에서 올라오는 애니메이션을 제공한다.
  - context와 route(MaterialPageRoute)를 매개변수로 받는다.
  - MaterialPageRoute는 builder를 사용할 수 있는데, StatelessWidget와 같은 위젯을 매개변수로 받는다.

## 6.10 정리
- Hero 위젯을 이용하여 애니메이션 효과 추가
  - 이전까지는 화면이 바뀌는 애니메이션으로 사용했다면 Hero 위젯은 해당 영역만 이동되는 것 처럼 보여주는 위젯이다.
  - Container 처럼 한 영역을 담당하는 위젯에 Wrap with Widget을 해서 Hero를 입력하여 사용하면 되고, 필수 파라메터는 tag이다.
  - tag에는 해당 영역에 고유값(id 등)을 받도록 해주면 된다.
