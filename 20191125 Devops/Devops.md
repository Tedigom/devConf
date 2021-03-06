# AWS KRUG Devops Session - 애자일 운동과 모던 개발 요소
#### 정도현(AWS)


DevOps에 기대하는 것? 
—> DevOps는 경쟁력을 갖추기 위한 강력한 도구 - 남들보다 빨리 출시하고, 안정적으로 돌릴수 있다.

Agile 소프트웨어 개발 선언

공정과 도구보다 / 개인과 상호작용을
포괄적인 문서보다 / 작동하는 소프트웨어를
계약 협상보다 / 고객과의 협력을
계획을 따르기 보다 / 변화에 대응하기를 가치있게 여긴다.


키친 나이트메어 -> 컨설팅이 끝나는 순간에는 해피엔딩으로 끝나지만,  방영후 몇년 뒤에는 많은 음식점들이 폐업한다.
마찬가지로, 기업도, 컨설팅이 끝나는 순간에는 문제가 해결되어 해피엔딩이지만, 얼마 뒤에는 더 큰 문제와 직면한다.

왜? 

문제라는 것은, 하나를 해결을 하면 그 상태가 유지되지 않는다. —> 문제는 문제를 낳는다.


#### 이러한 환경에서 우리가 갖춰야할 능력
1. 문제를 제대로 인식할 수 있는 능력
2. 시행착오를 겪더라도, 스스로 문제를 해결할 수 있는 능력



### 현대적인 개발요소

![d](https://github.com/Tedigom/devConf/blob/master/20191125%20Devops/modern.png)


1. Ownership 
-> Ownership은 내가 제안하거나, 내가 의도한 대로 일을 했을때 생기는 경우가 많다.
-> ‘이 일은 내것이다’ 라고 마인드셋을 갖추게 하는 것이 중요 
-> Ticket Driven Development : issue tracker 등의 일정관리 
-> Code Management System 
 
 Code review에는 두가지가 필요하다 - **Testcode가 제대로 짜여져있는가? + 가독성**

코드리뷰의 의미 - 원래 만든사람이 퇴사했을 때, 누구를 불러야 하나? - > 리뷰를 한 사람들

코드 리뷰의 의미 2 - 소프트웨어의 품질은 bottom 라인을 끌어올리는 것이 중요하다.( 잘하는 사람보다 못하는 사람들을 끌어올리는 역할) —> 코드리뷰는 단기간에 실력을 많이 끌어 올리는데에 효과가 있음.

2. Value
-> 회고(Retrospect)  : ‘개선’ 의 의미에서 굉장히 중요 감추려 하지말고, 드러내서 고쳐나가자!
-> Continuous Delivery - DevOps의 핵심 / 사람이 할수 있는 일은 사람이 , 기계가 할 수 있는 일은 기계가 (Test Automation이 반드시 자동화 되어야함)

TDD와 Test Automation은 엄연히 다르다.

TDD(테스트를 먼저 짜고, 로직을 만든다.)
TDD가 잘 적용되는 케이스  - 비교적 디자인이 명확한것 , 기존에 만들어 봤던것
TDD가 적용되기 어려운 케이스 - 처음 해보는 것, 만들어나가면서 고쳐야하는 것 —> 너무 많은 댓가를 치룸. 
**(로직이 완성되었을때,  테스트 코드가 완성이 되어있으면 충분하다.)**

3. High Availability / Fault Tolerance 
-> Cloud Computing과 Chaos Engineering이 큰 비중을 차지함


Netflix가 2014년 12월 24일 AWS에서 Region down을 겪음 - 큰 손실 이후 아키텍쳐를 바꾸어 나감 —> Chaos Engineering

Chaos monkey -> EC2를 랜덤하게 다운 시키면서 인스턴스 단위로 발생할 수 있는 장애를 감지, 극복
Chaos gorilla -> AZ down
Chaos kong -> Region down

Netflix - Production에서 Chaos Engineering을 진행하고 있음.  Down 되면 안되기 때문에 down을 시킴.
— 고가용성, 오류에 대한 내성을 높인다.

MSA -> Two Pizza Team -> Ownership 

반드시 필요한것 : Serverless Architecture

DDD - 마이크로 서비스를 디자인 하기위해서 ,현실세계를 어떻게 바라봐야하는가?



## 개발 + 운영 = 데브옵스

Waterfall의 치명적단점 - 서비스나 ,소프트웨어가 모양을 갖추면서 원하던 것이 이것이 아니라는 것을 알게됨. --> 완성품은 만족하기 힘듦

MVP 중심 -> 원하는 서비스를 맞춰나갈 수 있음.(높은 완성도) + 실패가 제한적으로 일어남.
설계와 테스트가 반복적으로 일어나기 때문에 일이 많음 —> 툴에 최대한 의존해야함.

DevOps -> 사람이 할 수 있는 일은 사람이 집중 / 사람이 하지 않아도 되는 일은 떠넘긴다는 개념이 중요함. ( 핵심 요소 )

