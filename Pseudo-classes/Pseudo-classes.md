# 가상클래스(Pseudo-classes)

선택자:가상클래스 {속성:속성값}으로 구성   
가상클래스의 이름은 대소문자를 구분하지 않지만 주로 소문자로 작성

``` 
selector:pseudo-class {property:value;}
```



## :link

* 방문하지 않은 링크에 스타일 적용
* default 파란색
``` css
a:link {}
```

## :visited
* 방문한 링크에 스타일 적용 
* default 보라색
``` css
a:visited {}
```

## :hover

* 특정 요소에 마우스를 올렸을 때 스타일 적용
* 퍼블리싱에서 굉장히 많이 사용

``` css
a:hover {}
```

## :active
웹 요소를 활성화(클릭) 했을 때 스타일을 적용 

``` css
a:active {}
```


## :focus
웹 요소에 초점이 맞추어 졌을 때 스타일 적용
* 텍스트 필드 안에 마우스를 올리거나 tab키를 눌러 커서를 이동 했을 때 스타일 지정
``` css
a:focus {}

```


## :target




## :enabled, :disabled



## :checked





## :fist-child


## :last-child

## :only-child

## :nth-child(n)
n에는 숫자 또는 수식을 넣는다.   
일반적으로 홀수, 짝수를 주로 사용하며 등차수열 수식을 만들어 넣기도 한다.
* 홀수 : odd, 2n+1
* 짝수 : event , 2n





## element:nth-of-type(n)







## :empty

:empty 가상클래스는 공백문자를 제외하고 자식이 없는 요소를 선택한다.
공백문자와, 자식 요소가 있다면 선택되지 않는다 

``` html 

<style>
.ex_01 p {width:100%;height:20px;border:1px solid #ccc}
.ex_01 p:empty {background:#fa1;}
</style>

<div class="ex_01">
    <p> </p>
    <p><span></span></p>
    <p></p><!-- //empty -->
    <p><!-- //empty --></p><!-- //empty -->
</div>


```





## :not()
```
input:not() {...}
```



## :is()
```
:is(h1,h2,p) {...}
```

## :has()
```
div:has(p) {...}
```


## :root 









[가상클래스 명세서] (https://drafts.csswg.org/selectors/ "이동")
