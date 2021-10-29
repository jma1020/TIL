# Nullish coalescing operator (null 병합 연산자)


```javascript
const name = 'mini'
const userName = namw || 'Guest'
// || or 연산자는 앞이 false 일 떄 뒤에 실행

//이런식으로 기본 값 설정시 많이 사용

```

하지만 위에 방식은 버그 발생가능!!
like 
    undefined, null 일 때 기존값 넣고 싶은데
    ''처럼 비어있을 때 , 숫자 0일때도 Guest로 설정이 됨

    --이름을 쓰고싶지않거나 0이 필요할 때 사용하면 안댐 !!!! 강제 Guest

### 개선방법
```javascript
const name =''
const userName = name ?? 'Guest'
const num = 0 
const userNum = num ?? 'undefined'

```

진짜 존재 안할때만 대체함   ((공백이랑 0은 해당 안되도록 개선한 방법))

 
### 추가설명))) || 연산자를 통한 기본값 처리의 문제점

그동안 자바스크립트에서는 주로 || 연산자(logical OR)를 사용해서 기본값 처리를 해왔는데, 이 방법은 한 가지 맹점이 있었습니다.


왜 이러한 오류가 발생하는 걸까요? 원인은 || 연산자는 자바스크립트에서 logical OR 구할 때 좌항이 falsy한 모든 경우에 우항을 선택하기 때문입니다. 자바스크립트에서는 undefined나 null 뿐만 아니라 false, 0, "", NaN 등 다양한 값들이 falsy가 될 수 있습니다.


따라서 || 연산자로 기본값을 처리하면 falsy에 의존하는 코드가 되어 잘못 사용하면 다음과 같이 상황에 따라서 의도치 않은 결과를 얻을 수 있습니다.

진짜 존재 안할때만 대체함   ((공백이랑 0은 해당 안되도록 개선한 방법))


### 추가설명))) ?? 연산자를 통한 견고한 기본값 처리

?? 연산자를 사용하면 nullish 즉, undefined와 null에 대해서만 기본값 처리를 할 수 있습니다.

?? 연산자는 다음과 같이 좌항이 undefined와 null이 아닌 경우에만 우항을 선택하며, 그 외의 경우에는 항상 좌항을 선택합니다.


### 더욱 첨가))) ?. 연산자와 함께 사용하기

?? 연산자는 ES2020에서 함께 도입된 ?. 연산자와 함께 사용하면 더욱 시너지를 발휘합니다. optional chaining을 위해 사용되는 ?. 연산자에 대한 내용은 관련 포스팅 참고.