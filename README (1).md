---
description: 2024 . 04 - 2024 . 05
---

# Baily 앱 서비스의 푸시 알림 기능 개발







### 개요

<figure><img src=".gitbook/assets/IMG_7160.jpg" alt=""><figcaption></figcaption></figure>

**Backend**

* NestJS
* Sequelize
* mySQL, Redis
* AWS SQS, EventBridge-scheduler



### 경험

EJN의 신규 서비스인 Baily 는 게임 친구를 찾을 수 있는 소셜 네트워킹 어플리케이션입니다. Baily의 2차 MVP 범위에 포함되었던 푸시 알림 서비스를 맡게 되어, React Native 의 라이브러리인 Expo notification 을 구현하였습니다. 알림 발송과, 발송이 잘 되었는지를 일정 시간 후에 확인하는 알림 워커를 별도로 작업하고, AWS SQS와 EventBridge-scheduler을 활용하였습니다.



### 성과 및 회고
