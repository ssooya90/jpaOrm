# setter와 bulider 차이

1. 생성자의 단점

파라미터가 많아질 경우 생성자 짐작이 어려움 (카운팅, 순서 변경 등)

ex Member(param1, param2, param3, param4, param5, param6 ...)

2. 자바빈즈 패턴

매개변수가 없는 생성자를 만든 후, setter 메서도를 통해 매개변수값 지정

```sql
TestVO testVO = new TestVO();

testVO.setUSerIdx(1);
testVO.setUserName("kimseohae");
testVO.setTitle("test");
testVO.setTitleA("test");
testVO.setTitleB("test");
testVO.setTitleC("test");
..
testVO.setTitleD("test");
```

1. 빌더패턴

위 1,2번의 단점을 개선한 것이 builder 패턴이다.

```sql
Test test = new Test
             .Builder()
             .userName("kimseohae")
             .userIdx(1)
             .title("hello")
             .build();
```