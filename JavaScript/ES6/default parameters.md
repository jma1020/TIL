# Default parameters (기본값 매개변수)

함수 매개변수에 기본값을 줄 수 있다.

```javascript 
function printMessage(message) {
    if(message == null){
        message = 'default'
    }
    console.log(message)
}

printMessage('hello')
printMessage()   //실행값 defeult

//이것을 이제 함수에서 기본값 설정
function printMessage(message = 'default')

```