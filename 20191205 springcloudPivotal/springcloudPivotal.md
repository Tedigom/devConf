# Pivotal meetup - 스프링 클라우드를 사용한 마이크로 서비스

Spring cloud setup :  1,2,3,4 shell file 순서대로 적용 
Pivotal web services : run.pivotal.io - cloud native platform 

Micro service의 outer architecture가 기존 넷플릭스 OSS 환경에서 아래와 같이 바뀌고 있음.(Reactive 기반 기술의 영향.(Reactive가 시장의 흐름이 됨)

현재 —> Replacement

Hystrix. —> Resilence4j 
Ribbon. —> Spring Cloud loadbalancer
Zuul1 —> spring cloud gateway …
Eureka —> Spring cloud Eureka


Reactive foundation에서 첫번째 프로젝트 조만간 1.0v 출시 ( R Socket)
R2DBC - mysql, postgesql, H2 등 지원

Spring cloud gateway 관련하여서는  [Spring Cloud Gateway](https://cloud.spring.io/spring-cloud-gateway/reference/html/) 찹조




## Spring Cloud Kubernetes
* JVM
왜 JDK가 container와의 궁합이 중요한가? - 
낮은 jdk(1.4,1.6…. ) 의 경우
Shared library는 OS의 메모리까지 다 씀. —> 메모리 조절과 관련하여 crash가 날 수 있음.

—> container에는 256m을 지정했지만, Java process는 실제로는 1GB를 사용하게 됨.

* Containerized image
    * Docker file -> docker build 
    * docker-maven-plugin
    * docker-gradle-plugin

    * JIB 사용—> docker image builder
    Gradle plugin —> com.google.cloud.tools.jib 추가
From , to 에 관련 정보를 넣는다.

ReadinessProbe / LivenessProbe
    
#### 
Kubernetes scheduler , scaling

LivenessProbe -> 쿠버네티스의 pod가 정상적인지 아닌지를 확인함.
어플리케이션이 죽엇을때 , restart

ReadinessProbe -> 처음 가동할때 ready상태가 되는지를 check
서비스 entry point에 서비스 ip를 넣는 역할을 함
언제 오픈을 할것인지를 정하는 역할


세미나 관련 상세 자료는 아래 페이지에서 
[GitHub - jupilhwang/meetups](https://github.com/jupilhwang/meetups)


