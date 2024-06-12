---
description: 2024 . 03 - 2024 . 04
---

# EZ TWIP 개발

{% embed url="https://www.cast.help/update/eztwip-release" %}

### 개요

이지트윕은 클릭 몇번으로 결제부터 후원까지 빠르게 진행할 수 있는 크리에이터 후원 기능입니다. \
기존 트윕의 메시지 후원에서 복잡한 옵션 선택을 간소화하였습니다.&#x20;

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/스크린샷 2024-06-12 오후 3.00.11.png" alt=""><figcaption></figcaption></figure>

### 개발환경

* NestJS
* Sequelize
* mySQL, Redis
* Youtube livechat api
* NestJS Cron
* Jest
* artillery



### 경험

#### 후원 로직 신규 작성

분리되어있던 후원과 결제 api를 통합하기 위해 redis 캐시와 redirect를 이용해 단일 api처럼 보이게 하였습니다.\
후원로직에 너무 많은 정보가 들어가있었는데, EZ TWIP에 필요한 부분만 남기고 코드를 정리했습니다. \
이전 후원 로직과 동일한 결과를 확인하기 위해 유닛 테스트와 스트레스 테스트를 활용하였습니다.

#### EZTWIP 챗봇기능 - Youtube livechat api 활용&#x20;

(챗봇이라기보단 채팅 서비스에 가깝습니다. )\
일정 시간마다 한번 씩 유튜브 채팅에 후원 페이지 주소를 보내줍니다. 또, 후원한 경우 크리에이터가 놓치지 않도록 후원 완료 메시지도 채팅창에 보내주는 기능입니다. \
Youtube livechat api - chat insert 와 NestJS Cron을 이용해서 10분에 한번씩, 방송이 켜져있고 설정을 해둔 사용자를 대상으로 채팅을 보내줍니다.&#x20;



### 성과

출시 이후 1달동안 50만원, 후원 건수 100건 돌파

