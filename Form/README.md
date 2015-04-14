# 폼 사용 예제

- 폼 사용
 - [폼 뷰 생성](./01_create_form_view)
 - [XML 룰셋 파일과 컨트롤러 액션 추가](./02_ruleset_and_controller_action)
 - [인사 메시지 출력](./03_print_hello_world)

폼은 사용자 입력값을 서버에 전송할 때 사용됩니다. XE에서는 폼을 전송할 때 입력값의 유효성을 확인하기 위한 룰셋 기능을 제공합니다. XE의 룰셋 기능을 사용하면 입력값의 유효성 확인 스크립트를 별도로 제작할 필요가 없습니다.

폼별로 다음과 같은 항목이 필요합니다.

- 폼 마크업과 설계
- 폼 전송 시 호출되는 서버 측 메서드

이와 같은 폼 전송을 위해서 연동하는 XE의 구성 요소는 다음과 같습니다.

- 폼 템플릿 파일: 폼의 레이아웃과 필드 정의
- 폼 전송을 처리할 controller 메서드(controller 파일 내)
- 폼 유효성 검사를 위한 룰셋 XML 파일