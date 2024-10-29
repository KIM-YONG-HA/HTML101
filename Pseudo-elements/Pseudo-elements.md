# 가상요소(Pseudo-elements)

## ::first-line

첫번째 줄에 스타일을 적용
```
p::first-line {...}
```

## ::first-letter
첫 번째 단어에 스타일을 적용

```
p::first-letter {...}
```


## ::before

요소 앞에 콘텐츠를 추가

```
div::before {content:""}
```

## ::after
요소 뒤에 콘텐츠를 추가

```
div::after {content:""}
```

## ::before, ::after 응용

* clearfix

```
.float_r::after {content:"";display:block;clear:both}
```


* 불릿

```

ul li {padding:0 0 0 10px;position:relative}  
ul li::before {content:"";width:10px;height:10px;background:url("/src/img/bullet.png") 0 0 no-repeat;position:absolute:left:0;top:0}   

/* 아래의 방식도 가능 */
ul li::before {content:url("/src/img/bullet.png")}  

```


* 뱃지(badge) : 불릿방식과 같으며 알림이 떴을 때 

```

ul li {padding:0 0 0 10px;position:relative}  
ul li.is_alarm:before {content:"";width:10px;height:10px;background:url("/src/img/bullet.png") 0 0 no-repeat;position:absolute:left:0;top:0}  

```

* 가상요소는 DOM 접근이 어렵기 때문에 토글 클래스로 처리하는게 편하다.

* 넘버링
    * ol의 list-style로 가능하나 들여쓰거나 내어쓸 수 있다.



## 세미콜론 개수

css2에서 :가상요소로 등장하였고 호환성 및 이전 버전의 일관성의 이유로 세미콜론 하나도 작동되지만 css3에서는 ::가상요소로 권장하고 있다.




