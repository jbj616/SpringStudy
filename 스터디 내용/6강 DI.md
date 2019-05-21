## 6강 DI

: 객체를 따로따로 분리해서 필요한 경우 붙이고 그렇지 않을경우 나누는 것

- 유연성있는 프로그램
- 의존 주입



일체형 - 생성자 주입

분리형 - 생성자 + setter



**스프링 컨테이너 생성 및 빈 객체 호출 과정**

스프링 설정 파일 -> 스프링 컨테이너 -> getBean() 객체 사용

- 스프링 컨테이너에서 객체들 Di 형성



studentAssembler->에서 studentDao객체를 생성하고 모든 객체에 studentDao 주입

- 모든 객체에서 studentDao를 사용

```xml
<constructor-arg ref = "studentDao"></constructor-arg>
```

studentDao를 주입하여 생성

```xml
<bean id = "registerService" class="ems.member.service.StudentRegisterService">
	<constructor-arg ref = "studentDao"></constructor-arg>
</bean>
```

