---

title:  "AWS NLB와 보안 그룹"

search: true
categories: 
  - AWS management diary
---


# AWS에서 NLB 사용시 궁금했던 점

NLB는 AWS에서 제공하는 로드밸런서 서비스 중 하나로 network단에서 사용한다.

사용하는 방식도 ALB랑은 다른 부분이 있다. 

가장 큰 차이점은 보안 그룹 설정시 NLB의 IP를 사용할 일이 없다는 것이다.

이 부분을 이해하기 힘들었다. 왜냐하면 NLB는 IP가 있기 때문이다.

stackoverflow를 뒤져본 결과 한 가지 글을 보게 되었는데 

[Why is it that an NLB in AWS does not require a Security Group?](https://stackoverflow.com/questions/63235672/why-is-it-that-an-nlb-in-aws-does-not-require-a-security-group)

NLB의 네트워크 인터페이스 콘솔에 들어가 보면 "소스/대상" 부분에서 아니오라고 되어있는 것을 확인 할 수 있다. 

근데 이건 NAT도 마찬가지랜다. 확인해 보니 실제로 그렇더라 그래서 NAT또한 SG 설정을 하지 않는다.

이 소스와 대상의 값이 SG를 사용하냐 마냐의 판가름 나는 것 아닌가하고 답변을 달아 주셨다. 

그리고 덩달아 기술적으로 못하는 것이 아니라 AWS의 의도일 수도 있다고 한다. 주 목적은 프락시!!! 도착지가 있어야지 SG를 쓰네 마네 한다고 한다. 

그리고 또 하나 궁금했던 점은 NLB를 통해 들어 올때는 대상의 SG로 inboud를 설정 하면 안되는 이유였다.

하단의 링크를 보면 ip나 VPC CIDR을 쓰도록 한다. 

[Register targets with your target group](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/target-group-register-targets.html)

그래서 AWS 측에다가 문의해 봤더니 NLB가 실제 노드가 아닌 클러스터 된 네트워크 장비이기 때문에 SG 가지고 있지 않아 그렇다고 한다. 

어찌보면 위에랑 같은 이유인 것 같다 즉 소스와대상이 없는 상태이기에 SG 요구하지 않고 그렇기 때문에 inbound에 넣지 않아도 되는?? 상황인 것 같다.

결론: NLB는 SG 설정 안해도 되고 네트워크는 넘나 어렵다.