# Spread syntax (전개 구문)

배열이나 문자열같이 반복 가능한 문자를 개별 요소로 분리하는 문법.
ex)
```javascript
console.log('mini')

//출력값 
m  i  n  i

```

추가로 공부해서 작성










state 배열 0번지 변경 원할 때
원본 state 는 수정 불가    ((특히 state 가 Array 나 Object  자료형이면))

그래서 state 의 복사본을 생성
var newArray = like;
newArray[0] = '여자코트 추천'
setLike(newArray)                  --이건 복사가 아니라 값 공유이다

근데 이렇게 복사하면 안되고
state를 deep copy 해서 수정해줘야함 
--> [...like]

deep copy 란 값공유x 하지않고  서로 독립적인 값을 가지는 복사 

... spread operator == 중괄호, 대괄호 둘다 다 제거를 해주세요라는 뜻  
그러면   usestate에 있는 중괄호가 제거가 된다 

그리고 다시 중괄호로 담는다.

리액트 대 원칙 : immutable data
직접 수정이 되면 안된다.
