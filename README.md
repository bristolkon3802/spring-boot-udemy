# Spring Boot

### @Primary vs @Qualifer
- @Primary: 여러 후보가 자격이 있을 경우, Bean에게 우선권을 주는 것.
            5개의 Bean이 있고, 그중 하나에 @Primary가 적용되었다면 해당 Bean이 우선권 적용.
- @Qualifier: 특정하게 지정된 Bean을 자동 와이어링 함.
- @Autowired: 가정 적합한 Bean을 달라고 요청.

> @Primary 와 @Qualifer 중에서 선택할 때는 항상 특정 의존선을 사용하는 클래스 관점에서 생각 후 사용. <br/>
> @Qualifer 가 @Primary 보다 더 높은 우선순위를 갖고 있음.

