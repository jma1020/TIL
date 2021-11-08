# FlexBox

이전에는 가운데 정렬하거나 동일한 간격, 높이으로 배치하고 안되었음
이걸 flex로 손쉽게 가능
 
 float 은 원래 이미지와 텍스트를 배치하는 용도 하지만 옛날에는 레이아웃기능이 없어서 float 을 써서 나눠서 배치했다((원래 목적이 xx)) 

## 중요 포인트 1
 container에 적용되는 속성값
    display
    flex-direction
    flex-wrap
    flex-flow
    justify-content
    align-items
    align-content


 item 적용되는 속성값
    order
    flex-grow
    flex-shrink
    flex
    align-self


## 중요 포인트 2

main axis 와 cross axis로 나뉜다

이 main axis는 direction 으로 축을 바꿔줄 수 있다



### 예제 

### flex-wrap 
기본값은  nowrap

아이템들이 많아지고 브라우저를 작게해도 한줄에 빼곡하게 붙어있다 
우리가 wrap핑을 안하겠다 지정해서 그럼 

wrap으로 바꾸고  아이템들이 한줄에 꽉차게되면 자동적으로 다음라인으로 넘어감 

wrap-reverse도 있음  그러면 거꾸로 wrap댐

### flex-flow 
이거는 direction 과 wrap을 합친것이다
border 로 한번에 지정하는 것과 같이!!

### justify-content

아이템들의 배치를 결정하는 요소
중심축에서 아이템을 어떻게 배치하는지 결정


flex-start , flex-end , center 
space-around , space- enenly , space-between 


### align-items

반대축에서 아이템을 배치하는 속성 cross axis

align-items는 **cross-axis를 기준으로 이동합니다.**

**align-content:** flex-container 의 cross-axis 축의 아이템들이 **여러줄** 일때 사용 가능합니다.

align-content는 corss axis에 대한 justify-content라 이해할 수 있다. 값도 space-between 처럼 justify-content 에서 사용되는 값을 줄 수 있다.

BUT!!
align-content는 nowrap인 경우 사용하는 의미가 없다. nowrap은 강제로 한 줄에 그리는 것이기 때문에 flex line이 하나 뿐이기 때문이다. 반대로 align-itmes는 line이 한 줄인 경우에도 그 라인 안에서 정렬하는 것이기 때문에 작동한다.


/* Basic keywords */
align-items: normal;
align-items: stretch;

/* Positional alignment */
/* align-items does not take left and right values */
align-items: center; /* Pack items around the center */
align-items: flex-start; /* Pack flex items from the start */
align-items: flex-end; /* Pack flex items from the end */

아이템 나열되는 위치를 지정

/* Baseline alignment */
align-items: baseline;
align-items: first baseline;
align-items: last baseline; /* Overflow alignment (for positional alignment only) */
align-items: safe center;
align-items: unsafe center;

/* Global values */
align-items: inherit;
align-items: initial;
align-items: revert;