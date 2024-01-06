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
