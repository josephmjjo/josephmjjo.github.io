---
title:  "Traceroute란"
search: true
categories: 
  - Network
---


Traceroute
패킷이 지나간 경로 파악 
특별한 패킷을 보내서 라우터에 도착할 때 마다 라우터의 주소와 이름을 소스에 역전송한다.
도착지까지 전송 되었을 땐 출발 지점 패킷으로 메세지를 역전송하기에는 넘 멀기에 
출발지에서 전송했을때와 메세지를 받았을 때의 시간을 기록한다.
즉 왕복 시간을 기록한다.
번호/이름(라우터 주소)/메세지 왕복 시간(3번 시도)
1 cs-gw (128.119.240.254) 1.009 ms 0.899 ms 0.993 ms
2 128.119.3.154 (128.119.3.154) 0.931 ms 0.441 ms 0.651 ms
3 border4-rt-gi-1-3.gw.umass.edu (128.119.2.194) 1.032 ms 0.484 ms 0.451 ms
4 acr1-ge-2-1-0.Boston.cw.net (208.172.51.129) 10.006 ms 8.150 ms 8.460 ms
5 agr4-loopback.NewYork.cw.net (206.24.194.104) 12.272 ms 14.344 ms 13.267 ms
6 acr2-loopback.NewYork.cw.net (206.24.194.62) 13.225 ms 12.292 ms 12.148 ms
7 pos10-2.core2.NewYork1.Level3.net (209.244.160.133) 12.218 ms 11.823 ms 11.793 ms
8 gige9-1-52.hsipaccess1.NewYork1.Level3.net (64.159.17.39) 13.081 ms 11.556 ms 13.297 ms
9 p0-0.polyu.bbnplanet.net (4.25.109.122) 12.716 ms 13.052 ms 12.786 ms
10 cis.poly.edu (128.238.32.126) 14.080 ms 13.035 ms 12.802 ms

throughput = 처리율이라고도 부른다. 통신에서 네트워크 상의 어떤 노드나 터미널로부터 또 다른 터미널로 전달되는 단위
서버에서 라우터 까지 전송률을 Rs라고 하고 라우터에서 클라이언트까지 Rc라고 할 때 
Rs+Rc의 throughput은 bit로는 fluid, communication link로는 pipes 라고 한다. 
bottleneck link 
병목 링크란 두개 이상의 링크 네트워크에서 가장 작은 값을 병목링크 전송률 값이라 한다.