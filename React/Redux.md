# 상태관리 라이브러리 Redux

### Redux 쓰는 이유 

1. props 문법 귀찮을 때 씁니다
    컴포넌트가 100개있으면 100번 props 를 해야함

    그러므로 Redux 

    설치시 state보관.js가 생성댐

2. state 변경 관리할 때 씁니다.

    상태관리가 용이하다
    state관리가 용이하다
    
    모든 컴포넌트들이 한 state를 변경하기 시작한다
    그러다가 갑자기 버그가 생김 --> 그러면 100만개 컴포넌트 다뒤져야해

    그래서 Redux를 쓰면 쉽게가능
    Redux를 사용하면
    state 수정방법을 다 집어넣는다 state보관.js(store.js, index.js)에 

    if 이거누르면 몸무게 +1 이런식으로 수정방법 생성
    그래서 컴포넌트들은 수정해달라고 요청만 할 수 있다 

    버그가 일어나면 무조건 state 보관.js (store.js )가 범인이니깐 추적이 쉽다

```javascript
 function reducer(state = weight , action) {
	if(action.type === '증가') {
	  state++;
	  return state
	} else if(action.type === '감소') {
	  state--;
	  return state
	} else{
	  return state 
	}
	}
```


이제 컴포넌트가 수정해달라는 요청을 하는 




```javascript
const dispatch = useDispatch()
	return (
	  <div>
		<button onClick={()=>{ dispatch({type : '증가'}) }}> 더하기 </button>
	  </div> 
```

dispatch 를 임폴트한다 npm 다운

요 redux 마음에 안들면 비슷한 라이브러리  MobX, Overmind.js, Recoil 
 
