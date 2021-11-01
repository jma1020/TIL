# Optional chaining ()

Optional chaining 의 역할

```Text
object를 타고 내려갈 때, 해당 key가 유효한지 아닌지를 체그해주면서 내려감.
중간에 유효하지 않은 key가 있으면, 에러를 뜨게 해서 시스템을 멈추게 하는게 아니라 undefined를 띄워서 표시해줌.
```

참고([https://ko.javascript.info/optional-chaining])


```javascript 
const person1={
    name:'mini'
    job : {
        title : 's/w',
        manager : {
            name:'bob'
        },
    },
}
//person1 = 직장이있고

const person2 = {
    name: 'bob'
}
//person2 = 직장이없음

function printManager(person) {
    console.log(person.job.manager.name)
}
//직장이 있고 매니저도 있어서 해당 매니저의 이름을 호출하는 함수이다
//perosn2 는 직장부터 없어서 에러가 생긴다


```

### 첫번째 개선안 

if문을 이용해 job과 manager가 null이 아닐때 조건을 줘서 에러방지가능

하지만 이것도 좀 그렇다

### 두번째 개선안 

Ternary operate를 사용

```javascript 
function printManager(person) {
    console.log(
        person.job
            ? person.job.manager
                ?person.job.manager.name
                : undefined
            :undefined
    )
}
```

### 세번째 개선안

And 연산자 사용

```javascript
function printManager(person) {
    console.log(person.job && person.job.manager && person.job.manager.name)
}

//하지만 너무 중복이야
```

### 네번째 개선안

Optional chaining 

```javascript
function printManager(person) {
    console.log(person.job?.manager?.name)
}
```



### 주의할 점
옵셔널 체이닝 문법 ?.은 세 가지 형태로 사용할 수 있습니다.

obj?.prop – obj가 존재하면 obj.prop을 반환하고, 그렇지 않으면 undefined를 반환함
obj?.[prop] – obj가 존재하면 obj[prop]을 반환하고, 그렇지 않으면 undefined를 반환함
obj?.method() – obj가 존재하면 obj.method()를 호출하고, 그렇지 않으면 undefined를 반환함
여러 예시를 통해 살펴보았듯이 옵셔널 체이닝 문법은 꽤 직관적이고 사용하기도 쉽습니다. ?. 왼쪽 평가 대상이 null이나 undefined인지 확인하고 null이나 undefined가 아니라면 평가를 계속 진행합니다.

?.를 계속 연결해서 체인을 만들면 중첩 프로퍼티들에 안전하게 접근할 수 있습니다.

?.은 ?.왼쪽 평가대상이 없어도 괜찮은 경우에만 선택적으로 사용해야 합니다.

꼭 있어야 하는 값인데 없는 경우에 ?.을 사용하면 프로그래밍 에러를 쉽게 찾을 수 없으므로 이런 상황을 만들지 말도록 합시다.