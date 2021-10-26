# Template literals

템플릿 리터럴이란 자바스크립트에서 문자열을 입력하는 방식입니다. 

템플릿 리터럴은 ES6에서는 백틱(back-tick)이라는 기호(`)를 사용하여 정의합니다.


백틱을 이용하게 되면 여러 줄에 걸쳐 문자열을 정의할 수도 있고, 자바스크립트의 변수를 문자열 안에 바로 연결할 수 있는 이점이 생깁니다

### 여러 줄에 걸쳐 문자열 선언하기

```javascript
var str = 'Template literals are string literals allowing embedded expressions. \n' + 
'You can use multi-line strings and string interpolation features with them. \n' + 
'They were called "template strings" in prior editions of the ES2015 specification.';

//원래는 이렇게 \n으로 중간중간 추가해주고 길어지면 + 를 계속 추가해줘야한다. 

const str = `Template literals are string literals allowing embedded expressions.
You can use multi-line strings and string interpolation features with them.
They were called "template strings" in prior editions of the ES2015 specification.`;

//백 틱 기호를 사용하면 번거로움이 없어짐
```

문자열 중간에 변수 바로 대입하기 

```javascript 

const weather = '날씨'

console.log('Today' + weather + '입니다')

//기존에 이렇게 추가하던걸

console.log(`Today ${weather} 입니다`)
```