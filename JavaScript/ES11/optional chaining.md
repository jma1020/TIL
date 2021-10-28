# Optional chaining ()

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
