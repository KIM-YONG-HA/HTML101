# CSS Animation
javascript를 사용하지 않고 css만으로 애니메이션 구현 가능


## 목차 
1. @keyframes
2. animation-name
3. animation-duration
4. animation-delay
5. animation-iteration-count
6. animation-direction
7. animation-timing-function
8. animation-fill-mode
9. animation 축약





# 1. @keyframes 
css에서 애니메이션 효과를 작성하기 위해서 @keyframes 키워드를 사용하여 작성한다

## @keyfames 작성1
from(시작), to(끝)을 이용하여 작성

``` css

@keyframes animationEffect {

    from {...}
    to {...}

}

```

## @keyfames 작성2
퍼센테이지를 이용하여 단계별로 작성

``` css

@keyframes animationEffect {

    0% {...}
    50% {...}
    100% {...}

}

```


## 2. animation-name 속성

animation-name 속성에는 @keyframe으로 지정한 애니메이션이름을 작성한다.

``` css
div {
animation-name:animationEffect;
}
```



## 3. animation-duration 속성
animation-duration 속성은 애니메이션이 완료되는 데 걸리는 시간을 지정하고 값이 지정되지 않으면 기본값이 0초이므로 애니메이션이 작동하지 않는다.

``` css
div {
animation-name:animationEffect;
animation-duration:1s;
}
```


## 4. animation-delay 속성

animation-delay 속성는 애니메이션 시작시간을 지연한다.
음수 값으로도 지정이 가능한데 n초 만큼 시작한 효과를 낼 수 있다.


``` css
div {
animation-name:animationEffect;
animation-duration:1s;
animation-delay:0s;
}
```



## 5. animation-iteration-count 속성
animation-iteration-count 속성은 애니메이션을 실행할 횟수를 정수로 지정한다.   
횟수가 무제한일 경우 **infinite**를 사용


``` css
div {
animation-name:animationEffect;
animation-duration:1s;
animation-delay:0s;
animation-iteration-count:4;
}
```



## 6. animation-direction 속성

animation-direction 속성은 애니메이션을 앞으로, 뒤로 또는 교대로 재생할지 여부를 지정한다.

* normal : 정상적으로(앞으로) 작동(default값)
* reverse : 역방향(뒤로)으로 재생
* alternate : 앞으로 재생 후 뒤로 재생(normal + reverse)
* alternate-reverse : 뒤로 재생 후 앞으로 재생(reverse + normal)


``` css
div {
animation-name:animationEffect;
animation-duration:1s;
animation-delay:0s;
animation-iteration-count:4;
animation-direction:alternate;
}
```


###  6-1. animation-direction 작동 순서

``` css

@keyframes radiusEffect{

    from {border-radius:0;}
    to {border-radius:50%;}

}

```

### 6-1-1. animation-direction:normal일 때

``` css 

div {
animation-name:radiusEffect;
animation-duration:1s;
animation-delay:0s;
animation-iteration-count:4;
animation-direction:alternate;
opacity:1;

}

```








## 7. animation-timing-function 속성


animation-timing-function 속성은 애니메이션의 속도 곡선을 지정한다.

* ease : 느리게 시작 -> 빠르게 진행 -> 느리게 끝(default값)
* linear : 시작부터 끝까지 동일한 속도
* ease-in : 느리게 시작
* ease-out : 느리게 종료
* ease-in-out : 느린 시작과 느린 종료
* cubic-bezier(n,n,n,n)- 3차 베지어 함수에서 원하는 값을 지정


``` css
div {
animation-name:animationEffect;
animation-duration:1s;
animation-delay:0s;
animation-iteration-count:4;
animation-direction:alternate;
animation-timing-function:linear;
}
```




## 8. animation-fill-mode 속성 

animation-fill-mode 속성은 애니메이션이 재생되지 않을 때(시작 전, 종료 후, 둘 다) 대상 요소에 대한 스타일을 지정한다.

* none : 실행 전이나 실행 후에 요소에 스타일을 적용하지 않음(default값)

* forwards : 마지막 키 프레임에 의해 설정된 스타일 값을 유지
    * 애니메이션 방향 및 애니메이션 반복 횟수에 따라 다르다

* backwards : 첫 번째 키프레임에 의해 설정된 스타일 값을 가져오고       애니메이션 지연 기간 동안 이를 유지.
    * 애니메이션 방향에 따라 달라짐 가져오는 스타일 값이 다름

* both : 애니메이션 앞뒤 모두에 대한 규칙을 따르며 애니메이션 속성을 양방향으로 확장.








## 9. animation 축약

animation 속성들이 익숙해진 상태라면 animation으로 축약이 가능하다.


애니매이션을 적절히 이용하면 인터랙티브한 웹페이지 구현이 가능하다.
