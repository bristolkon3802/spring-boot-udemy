# Spring Boot

### Java 객체를 생성하고 관리 - 에노테이션
- @Componet: Bean을 생성하려면 @Componet를 적용.
  > @Component를 클래스에 추가하는 경우, 클래스의 인스턴스는 Spring 프레임워크가 관리 함.<br/>
  > @Component는 Spring 프레임워크의 가장 중요한 어노테이션 중 하나인데,<br/>
  > @Component를 추가할 때마다 특정 클래스가 컴포넌트 스캔에 있다면 해당 클래스의 인스턴스, 즉 Spring Bean이 생성되고 프레임워크에 의해 관리됨.
  
- @ComponentScan: 자동으로 컴포넌트를 스캔.
  > Spring 프레임워크에 @Component를 검색 후 위치를 알려줘야 하는데, @ComponentScan를 사용.
  > @ComponentScan("packages.name") 이름을 명시적으로 지정하여 사용 가능.
  
- @Primary: 여러 후보가 자격이 있을 경우, Bean에게 우선권을 주는 것.
            5개의 Bean이 있고, 그중 하나에 @Primary가 적용되었다면 해당 Bean이 우선권 적용.
- @Qualifier: 특정하게 지정된 Bean을 자동 와이어링 함.
- @Autowired: 가정 적합한 Bean을 달라고 요청.

> @Primary 와 @Qualifer 중에서 선택할 때는 항상 특정 의존선을 사용하는 클래스 관점에서 생각 후 사용. <br/>
> @Qualifer 가 @Primary 보다 더 높은 우선순위를 갖고 있음.

- @Autowired: 의존성 추가
  > Spring Bean에 대한 의존성의 와이어링 프로세스를 말함.
  > Spring이 특정 Bean을 만나면 Bean이 필요한 의존성이 무엇인지 식별하려고 함.
  > 식별 후 의존성이 필요하다고 파악되면, 찾아서 생성자 주입을 통해 자동 와이어링 함.
  

### Spring Framework 고급기능
- @Lazy: (지연초기화) Bean을 지연하여 초기화할지 여부를 나타냄.
  > @Componet를 사용하는 모든 클래스나 Bean에 어노테이션을 적용한 모든 메서드에서 Lazy를 사용. <br/>
  > @Lazy 어노테이션을 지정하지 않는 한, 각각의 Spring Bean은 시작할 때 즉시 초기화 됨. <br/>
  > 권장하지는 않고, 자주 사용되지 않음. <br/>
  > 보통 즉시 초기화를 사용.
  
         
