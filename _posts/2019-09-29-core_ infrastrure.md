---
title:  "구글 클라우드 기본 용어"
search: true
categories: 
  - Cloud, Kubernetes, GCP
---

Zone이란 구글 클라우드 플랫폼 자원을 위한 배치 지역이다

Google Stackdriver란 여러 클라우드에서 사용한 워크로들 모니터하는 기능이다..

***

FIDO란 (Fast IDentity Online)의 약자로 홍채나,정맥등의 생체정보를 인증하는 방식이다.

***
U2F란 usb나 nfc 디바이스를 이용한 강력하고 단순한 2단계 인증의 개방형 표준이다.

*** 
IAM이란 (Identity and Access Manage)의 약자로 클라우드내에서 사용자마다 어떤 일을 할 수 있을지 권한을 주고 관리하는 것이다. 

google cloud platform 자원 상속 
서비스와 API들은 한 프로젝트 안에서 사용 가능하다.
Google은 고객의 보안의 모든 측면을 관리하지는 않는다.
2가지 이상 프로젝트에 정책을 공유하고 싶을때는 정책을 복사하기 보다는 정책이 들어있는 폴더에 프로젝트를 넣으면 된다. 

role이란 역할이라는 의미로 구글 클라우드에서는 owner, editor, viewor 그리고 billing administrator로 총 4가지이다. 
editor는 앱 전시, 코드 수정 서비스 설정등을 하고 viewer는 읽기만 가능하다.
owner는 editor가 하는 모든 걸 할수 있고 거기에 roll관리, 자워 허가도 가능하다. 프로젝트의 자원관리를 제외한 청구관리는 billing daministrator가 역할을 한다. 