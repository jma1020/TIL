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

## align-items

한줄일때 
 
/* Basic keywords */
align-items: normal;
align-items: stretch;

/* Positional alignment */
/* align-items does not take left and right values */
align-items: center; /* Pack items around the center */
align-items: flex-start; /* Pack flex items from the start */
align-items: flex-end; /* Pack flex items from the end */


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


## align-content

2줄이상일 때 

align-content: center;     /* Pack items around the center */
align-content: start;      /* Pack items from the start */
align-content: end;        /* Pack items from the end */
align-content: flex-start; /* Pack flex items from the start */
align-content: flex-end;   /* Pack flex items from the end */

/* Normal alignment */
align-content: normal;

/* Baseline alignment */
align-content: baseline;
align-content: first baseline;
align-content: last baseline;

/* Distributed alignment */
align-content: space-between; /* Distribute items evenly
                                 The first item is flush with the start,
                                 the last is flush with the end */
align-content: space-around;  /* Distribute items evenly
                                 Items have a half-size space
                                 on either end */
align-content: space-evenly;  /* Distribute items evenly
                                 Items have equal space around them */
align-content: stretch;       /* Distribute items evenly
                                 Stretch 'auto'-sized items to fit
                                 the container */

/* Overflow alignment */
align-content: safe center;
align-content: unsafe center;

/* Global values */
align-content: inherit;
align-content: initial;
align-content: unset;



# item의 속성값들

### order

### flex-grow

이게 없으면 원래 사이즈를 유지하고 있는다  근데,
컨테이너(브라우저)가 너무 작아지만 어쩔수없이 한줄에 꽉채우기위해 
작아지게 된다

flex-grow:1
하지만 flex-grow 를 쓰게되면 컨테이너를 채울려고 아이템들이 늘어나게 된다

flex-grow:2 
이것을 하게되면 1로 지정한 애들보다 2배로 커지게 된다 

and **더 늘어나지 않도록 만들 때 사용도 함**


### flex-shrink 

컨테이너가 작아졌을 때 어떻게 행동하느냐 지정하는 것 

flex-shrink
컨테이너 줄어들떄 더 줄어듬 
수치는 grow와 비슷하게 움직임 줄어든다는 의미로 

and **더 줄어들지 않도록 만들 때 사용도 함**   0으로 지정
### flex-basis
아이템의 기본 크기를 지정합니다. flex-grow나 shrink로 늘어나거나 줄어들기 전의 기본 크기를 설정합니다.

flex-direction이 row라면 basis는 가로, column이면 세로를 의미합니다.

**자식요소에 사용합니다!**  flex item 들의 크기를 특정합니다. width, height 와 다른점은 axis 방향에 따라 달라진다는 것 그리고 내부의 컨텐츠에 따른 유연한 크기입니다. 기본값은 auto. auto 일때는 width, height 값을 사용합니다.

만약 flex-basis 값이 적용되어 있다면 width, height 값은 무시됩니다.

### flex 

flex : grow shrink basis 의 축약형


### align-self 

컨테이너에서 배치할 수 있다면 item에서는 이걸로 아이템별로 정렬할 수 있다

item 하나만 center로 배치도 가능 




