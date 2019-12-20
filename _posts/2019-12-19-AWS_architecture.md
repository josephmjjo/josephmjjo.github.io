---
title:  "AWS architect"
search: true
categories: 
  - Network
---
__엘라스틱 서치__ 
Apache Lucence(아파치 루씬) 기반의 Java 오픈소스 분산 *검색* 엔진

__CDN__ 
Content Delivery Network의 약어로서 전 세계에 전략적으로 분산되어있는 서버 네트워크입니다. CDN은 사용자가 리소스를 다운로드 할 수 있는
대체 서버 노드를 제공하여 작동. 이러한 노드는 전 세계에 퍼져있음  예를 들어 미국에 있는 사용자가 중국 컨텐츠를 가져올때 중국에 있는 서버에서 
바로 가져오면 시간이 오래걸린다. 그래서 미국에 있는 CDN 서버에 복사를 하고 미국에 있는 사용자는 CDN 서버를 이용하면 된다. 그러면 대기 시간을 줄이고 
사이트 로딩을 빠르게 제공 할 수 있다. 
CDN 노드의 목적은 사이트의 정적 컨텐츠(이미지,css/js 파일, 구성요소 )를 캐시하는 것이다. 
더 깊이 알려면 GSLB 공부
Amazon CloudFront는 위어 언급한 CDN이라 생각하면 된다..html, .css, .js 및 이미지 파일과 같은 정적 및 동적 웹 콘텐츠를 사용자에게 더 빨리 배포하도록 지원하는 웹 서비스
<br>

__ECR이란__ 
Amazon Elastic Container Registry의 약자로 개발자가 Docker 컨테이너 이미지를 손쉽게 저장, 관리 및 배포할 수 있게 해주는 완전관리형 Docker 컨테이너 레지스트리입니다.
Amazon ECR은 ECS와 통합되므로 개발에서 프로덕션까지의 워크플로를 간소화할 수 있다.
<br>

__CodeDeploy__ 
Amazon EC2 인스턴스, 온프레미스 인스턴스, 서버리스 Lambda 함수 또는 Amazon ECS 서비스로 애플리케이션 배포를 자동화하는 배포 서비스
<br>
- code 
- 서버리스 AWS Lambda 함수
- 웹 및 구성 파일
- 실행 파일
- packages
- 스크립트
- 멀티미디어 파일
<br>

__codecommit__ 
Private git repository 서비스로 aws 에서 git을 관리해주는 서비스라 생각하면 된다.
<br>

__WAF__ 
웹 어플리케이션 방화벽으로 가용성에 영향을 주거나, 보안을 위협하거나, 
리소스를 과도하게 사용하는 일반적인 웹 공격으로부터 웹 애플리케이션이나 API를 보호한다.
