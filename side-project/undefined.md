# 달대표: 우리 동네 배달 대표

{% embed url="https://github.com/yujiniii/DeliveryDelegate-back" %}

4학년 졸업작품에서 "달대표" 앱의 서버를 맡아 node.js Express로 영수증 리뷰 파트를 구현하였습니다. 또 과거 동아리 대표 경험을 살려, 팀장으로서 기획, 발표, 보고서 작성 등을 문제없이 진행하였습니다.

### 기능 소개

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* #### **동네 주민 배달 대행**
  1. 위치 기반으로 같은 동네 주민 인증
  2. 배달 대표(이하 달대표) 를 정하는 미니게임 수행
  3. 수령한 음식을 나눠줄 랜드마크 설정 후 달대표가 음식 수령 및 배부

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

* **영수증 리뷰**
  1. OCR기술을 활용한 영수증 문자 인식
  2. 영수증의 주소 및 상호명과 위치 정보 비교
  3. 기존 리뷰에 타 사용자가 좋아요 표시 가능
  4. 누적 리뷰 10회마다 배달 대표 면제권 제공

#### 기술 스택

* **client**
  * android
* **server**&#x20;
  * Node.js Express&#x20;
  * MySQL sequelize
  * JWT&#x20;
  * crypto&#x20;
  * socket.io&#x20;
  * naver map API&#x20;
  * google vision API (OCR)
  * Docker&#x20;

### 성과

2022학년도 스마트 프로젝트 경진대회 장려상 (2022.11)

2022학년도 소프트웨어 프로젝트 설계 경진대회 우수상 (2022.06)

