# CSS 함수


## CSS 변수 선언

홈페이지 color system이 있다면 변수로 저장해서 사용할 수 있고 유지보수에 유리하다.  

:root {변수명:속성값}으로 작성하며 변수명 앞에는 하이픈 두 개(--)로 시작해야한다. 변수명에는 하이픈, 언더바 사용가능하다.

```
--font_size:16px;
--font-size:16px;
```

```
:root {
--main-txt-color:#333;
--sub-txt-color:#555
--main-bg-color:#ddd;
--common-border-color:#fafafa;
}
```

## val()

val(변수명) 함수로 값을 지정할 수 있다.

```
h2 {color:val(--main-txt-color)}
p {color:val(--sub-main-color)}
section {background:val(--main-bg-color)}
div {border-color:val(--common-border-color)}
```


## calc()
calculation 함수에 값은 크기나, 각도, 시간 백분율, 숫자 등 가능  
너비를 계산할 때 자주 사용한다.

```
div {width:calc(100% - 100px)}
```
* div요소 100%에서 -100px을 뺀 값을 계산한다.
* 사칙연산자(+, -, *, /) 사용 가능
* 피연산자는 숫자만 가능
* 연산자 사이에 띄어쓰기 필수
* 0으로 나눌 수 없다.




## min()

min() 함수는 괄호 안에 나열된  값 중에서 가장 작은 값을 적용한다.

```
min(value1, value2, ...)
```

```
img {width:min(50%, 400px);}
```


## max()
max() 함수는 괄호 안에 나열된  값 중에서 가장 큰 값을 적용한다.

```
min(value1, value2, ...)
```

```
img {width:min(50%, 400px);}
```


## clamp()

clamp() 함수는 값의 범위를 고정 및 제한한다

```
clamp(최솟값, 최적값, 최댓값)
```

```
p {font-size:clamp(1rem, 1vw, 2em);}
```



