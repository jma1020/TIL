# Ternary operator (삼항 조건 연산자)

REACT에서는 IF 절을 사용하는데 제약이 많다. 그래서, 삼항 연산자가 그 역할을 대신해야 한다. 
그런 이유로, 본격적으로 REACT를 들어가기 전에 삼항 조건 연산자에 대해서 알아보자!

## (조건식 ? 연산식1 : 연산식2)
:조건식의 결과값이 참이면 연산식1, 거짓이면 연산식2를 실행하라 

```javascript
const isCat = true
let component
if(isCat) {
    component ='고양이'
} else {
    conponent = '개'
}

//결과값  고양이  
//이렇게 쓰던걸 삼항조건연산자로

const component = isCat ? '고양' : '개'
```

### 우리는 왜 삼항 연산자를 사용해야 하는 걸까???

case1 가장 큰 이유는 코드의 간결성 때문이다.

case2 삼항 연산자는 중첩해서 쓸 수도 있다.   ((하지만 이렇게 쓰는 코드는 별로 추천하지 않는다.))
