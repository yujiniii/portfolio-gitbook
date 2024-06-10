# TWIP 2.0 마이그레이션

## 대시보드 2.0 마이그레이션 작업

{% embed url="https://www.cast.help/twip/twip-dashboard" %}

기존에 php codeigniter 로 작성된 TWIP 대시보드를 클라이언트-서버 구조로 마이그레이션하는 작업에 NestJS 백엔드 작업에 참여하였습니다.&#x20;

* NestJS, MySQL, Sequelize, class-transformer, swagger

## TWIP YOUTUBE 데이터 영구 저장 기능 구현

<figure><img src="../.gitbook/assets/스크린샷 2024-05-30 오전 2.50.11.png" alt=""><figcaption></figcaption></figure>

유튜브 채팅을 통해 가져오는 supers, 즉 유료이벤트들을 DB에 기록하는 내용입니다. 기존에는 DynamoDB에 임의로 저장한 형태라, 통계나 TWIP 대시보드에서 활용하기 어려웠습니다. 이벤트가 발생했을 때, 주 데이터베이스(MySQL)에 저장하도록 하였습니다. \
이를 통해 대시보드 통계 범위가 확장되어 사용자에게 더 다양하고 편리한 기능을 제공할 수 있었습니다.

기존 코드를 복사하는 형태로 작업할 수도 있었지만, 나중 작업자가 신경써야하는 범위를 줄일 수 있도록 코드 개선을 함께 진행했습니다. 사용하지 않던 타입을 새롭게 정의하고, 여러 앱에 걸쳐 중복되어있는 코드부를 하나의 앱에서 책임지도록 수정했습니다. \
이 작업을 토대로 새로운 이벤트 추가나 수정이 간편해졌고, 그때 꼼꼼히 읽은 youtube livechat 문서를 기억하며 다른 펑션이나 팀에서 물어보는 질문에 빠르게 답을 줄 수 있게 되었습니다.

* NestJS, MySQL, Sequelize, Youtube livechat api, Redis pub/sub

## TWIP 네이버 카카오 신규가입 구현

{% embed url="https://www.cast.help/update/twip-newaccount" %}

<figure><img src="../.gitbook/assets/스크린샷 2024-06-10 오후 3.07.42.png" alt=""><figcaption></figcaption></figure>

작업 전 네이버 로그인의 경우 신규 가입은 불가하고 기존 계정 연동만 가능한 상태였는데,네이버 신규 가입이 가능하게끔 코드 일부를 수정하였습니다. 카카오 간편 로그인 기능 구현하여 신규가입과 기존 계정 연동을 가능하게끔 하였습니다. 커스텀 인터페이스를 활용해 클래스에 규칙을 제공하는 방식과 strategy를 좀 더 유연하게 다루는 방법을 익혔습니다

* NestJS, MySQL, Sequelize, strategy, passport

