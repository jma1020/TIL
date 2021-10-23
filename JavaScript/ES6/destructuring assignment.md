# Destructuring assignment (구조분해 할당)

구조 분해 할당문법은 '배열' 혹은 '객체' 에서 각각  값(value)이나 프로퍼티(property) 를 
분해하여 손쉽게 별도의 변수에 담을 수 있도록 해 줍니다.

참고([https://ko.javascript.info/destructuring-assignment],[https://chanhuiseok.github.io/posts/js-10/])


### 객체에서 구조 분해 할당

객체에서 구조분해할당은 정말 정말 많이 쓰이는 문법입니다, 객체 내부의 프로퍼티 값을 간편하게 분해해서 
변수에 저장할 수 있게 해 줍니다 

사용할 변수명과 객체의 프로퍼티(키)가 같아도 된다면 아래와 같이 사용한다.
```javascript 
const student = {
    name: 'mini',
    level:1
}

const name = student.name
const level = student.level

//기존에 이렇게 하나하나 대입하는것을 -->

const {name, level} = student;

console.log(name)
console.log(level)
```
또한 값은 가져오고 싶지만 프로퍼티(키)와 다른 변수명을 가지고 싶을 때도 가능하다 

```javascript
const {name:studentNamem, level:studentLevel} = student

console.log(studentName)
console.log(studentLevel)

```


### 배열에서의 구조 분해 할당 

구조 분해 할당이라고 해서 특별한 문법적 형태가 다른 것이 아니라, 아래처럼 할당받을 변수를 왼쪽에, 분해할 대상을 오른쪽에 해서
대입하는 형식으로 작성하면 됩니다.

```javascript
    let [a,b] = [10,20]

    console.log(a) //10
    console.log(b) //20
```

또한 아래와 같이 미리 저장해 둔 배열로부터 구조 분해 할당하는 형태도 당연히 가능합니다.

```javascript
const animals = ['강아지','고양이']

const first = animals[0]
const second = animals[1]
//이렇게 하나하나 대입해주는걸 

const [first, second] = animals

console.log(first) //강아지
console.log(second) //고양이
```
또한 배열은 중간에 끼고 싶지 않은 값이 있다면

```javascript
const number = [1,2,3,4,5]
//여기서 2와 4,5 변수에 담고싶지 않을 때
const [first,,three] = number
//이렇게 ,,로 비워두면 2자리를 비우고 뒤에있는 변수는 작성하지 않으면 저절로 담기지않고 누락된다
console.log(first)
console.log(three)
```