---
description: 2023 . 06 - 2024 . 05
---

# TWIP TTS 관리 및 멜로디보이스 개발

### TWIP 메시지후원 TTS 관리

TWIP 메시지후원에 사용되는 모든 TTS에 대해 추가/퇴역 작업을 담당하였습니다.&#x20;

기존에 php ec2로 ssh접속해서 직접 수행하던 스크립트를 NestJS 에서 api를 통해 간단하게 실행할 수 있게끔 마이그레이션하였습니다.\
대규모 DB변경 스크립트를 API 요청으로 그대로 옮기자 timeout 이슈가 생겼습니다. 이 해결을 위해 Redis pub/sub을 사용하여 api 요청이 들어오면 publish 후 응답하고, 나머지는 subscribe 한 매서드가 처리하게끔 로직을 변경하였습니다.

* NestJS, mySQL, Sequelize, Redis pub/sub



### TWIP 멜로디보이스

(2023.11\~2023.12 / 2023.02)

{% embed url="https://youtu.be/eK5U8vRHO8Q?si=wRrFQ7oyX6rwl2Gh" %}

{% embed url="https://www.cast.help/update/melody-voice" %}

{% embed url="https://www.cast.help/update/melody-release" %}

외부 업체와 컨택하며 신규 TTS 엔진사를 도입하였습니다. 관련해서 대시보드, 유료화를 추가하면서 기존 서비스에 문제 없게끔 신경썼습니다.\
AWS EC2 1개에서 돌고있는 php 서버 1개로 전체 TTS 가 관리되는 형태였는데, 추후 마이그레이션을 고려하여 별도 NestJS 앱에 실제 API 구현을 작성하였습니다.  그 후 php 서버와 NestJS앱을 내부주소 cURL로 연결하였습니다.&#x20;

* PHP, NestJS, axios

통계가 기록되기 시작한 10월 말부터 멜로디 보이스를 선택해서 후원한 횟수는 13,802회 입니다. (유료화 전 1월 기준)
