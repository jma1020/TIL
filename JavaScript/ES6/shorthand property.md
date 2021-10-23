# shorthand property (객체 초기자)

객체의 키와 변수에 value가 같다면 축약가능

ex)
```javascript
const name = 'mini'
const age = '26'

const miniObject = {
    name : name,
    age : age
}

//이것을 축약해서 사용가능

const miniObject2 = {
    name,
    age
}


