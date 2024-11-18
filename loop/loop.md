# loop

배열의 데이터를 꺼낼 때 for, for of, foreach 예제


## 1차원 배열
### for문

``` javascript

let arr = ["가","나","다","라"];

for(let i=0;i<arr.length;i++){

    console.log(arr[i]);

}

```

### for of문
``` javascript

let arr = ["가","나","다","라"];

for(let el of arr){

    console.log(el);

}

```



### forEach 메서드
``` javascript

let arr = ["가","나","다","라"];

arr.forEach(function(el, idx){

    console.log("arr[" + idx "] = " + el);

})
  
```


### 결과

```
가
나
다
라
```






## 2차원 배열

### for문

``` javascript:;

let arr = [

    ["서울시청","https://www.seoul.go.kr/"],
    ["경기도청","https://www.gg.go.kr/"],
    ["제주도청","https://www.jeju.go.kr/"],
    ["강원도청","https://state.gwd.go.kr/"]

];


for(let i=0;i<arr.length;i++){

    console.log("기관명 : " + arr[i][0]);
    console.log("누리집 : " + arr[i][1]);

}


```

### for of문
``` javascript:;

let arr = [

    ["서울시청","https://www.seoul.go.kr/"],
    ["경기도청","https://www.gg.go.kr/"],
    ["제주도청","https://www.jeju.go.kr/"],
    ["강원도청","https://state.gwd.go.kr/"]

];


for(let el of arr){

    console.log("기관명 : " + arr[0]);
    console.log("누리집 : " + arr[1]);

}


```

### forEach 메서드

``` javascript:;

let arr = [

    ["서울시청","https://www.seoul.go.kr/"],
    ["경기도청","https://www.gg.go.kr/"],
    ["제주도청","https://www.jeju.go.kr/"],
    ["강원도청","https://state.gwd.go.kr/"]

];


arr.forEach(function(el, idx){

    console.log("기관명 : " + el[0]);
    console.log("누리집 : " + el[1]);

})


```


### 출력결과

```
기관명 : 서울시청
누리집 : https://www.seoul.go.kr/
기관명 : 경기도청
누리집 : https://www.gg.go.kr/
기관명 : 제주도청
누리집 : https://www.jeju.go.kr/
기관명 : 강원도청
누리집 : https://state.gwd.go.kr/
```



## 객체 배열 (Object Array)


### for문

``` javascript

let arr = [

    {
    orgname:"서울시청", 
    url:"https://www.seoul.go.kr/", 
    latitude:"37.56677014701592", 
    longitude:"126.97867491234639"
    },

    {
    orgname:"경기도청", 
    url:"https://www.gg.go.kr/", 
    latitude:"37.28893135508412", 
    longitude:"127.05347693534611"
    },

    {
    orgname:"제주도청", 
    url:"https://www.jeju.go.kr/", 
    latitude:"33.48889985012181", 
    longitude:"126.49822386525447"},

    {
    orgname:"강원도청", 
    url:"https://state.gwd.go.kr/", 
    latitude:"37.88530735666828", 
    longitude:"127.72982257639035"
    }

];


for(let i=0;i<arr.length;i++){

console.log("기관명 : " + arr[i].orgname);
console.log("누리집 : " + arr[i].url);
console.log("위도 : " + arr[i].latitude);
console.log("경도 : " + arr[i].longitude);


}



```


### for of문

``` javascript

let arr = [

    {
    orgname:"서울시청", 
    url:"https://www.seoul.go.kr/", 
    latitude:"37.56677014701592", 
    longitude:"126.97867491234639"
    },

    {
    orgname:"경기도청", 
    url:"https://www.gg.go.kr/", 
    latitude:"37.28893135508412", 
    longitude:"127.05347693534611"
    },

    {
    orgname:"제주도청", 
    url:"https://www.jeju.go.kr/", 
    latitude:"33.48889985012181", 
    longitude:"126.49822386525447"},
 
    {
    orgname:"강원도청", 
    url:"https://state.gwd.go.kr/", 
    latitude:"37.88530735666828", 
    longitude:"127.72982257639035"
    }

];


for(let el of arr){

console.log("기관명 : " + el.orgname);
console.log("누리집 : " + el.url);
console.log("위도 : " + el.latitude);
console.log("경도 : " + el.longitude);

}


```



### forEach 메서드

``` javascript

let arr = [

    {
    orgname:"서울시청", 
    url:"https://www.seoul.go.kr/", 
    latitude:"37.56677014701592", 
    longitude:"126.97867491234639"
    },

    {
    orgname:"경기도청", 
    url:"https://www.gg.go.kr/", 
    latitude:"37.28893135508412", 
    longitude:"127.05347693534611"
    },

    {
    orgname:"제주도청", 
    url:"https://www.jeju.go.kr/", 
    latitude:"33.48889985012181", 
    longitude:"126.49822386525447"},

    {
    orgname:"강원도청", 
    url:"https://state.gwd.go.kr/", 
    latitude:"37.88530735666828", 
    longitude:"127.72982257639035"
    }

];


arr.forEach(function(el, idx){

console.log("기관명 : " + el.orgname);
console.log("누리집 : " + el.url);
console.log("위도 : " + el.latitude);
console.log("경도 : " + el.longitude);

});


```




### 출력결과

```
기관명 : 서울시청
누리집 : https://www.seoul.go.kr/
위도 : 37.56677014701592
경도 : 126.97867491234639
기관명 : 경기도청
누리집 : https://www.gg.go.kr/
위도 : 37.28893135508412
경도 : 127.05347693534611
기관명 : 제주도청
누리집 : https://www.jeju.go.kr/
위도 : 33.48889985012181
경도 : 126.49822386525447
기관명 : 강원도청
누리집 : https://state.gwd.go.kr/
위도 : 37.88530735666828
경도 : 127.72982257639035
```



## 성능 차이 

1. for 문
반복 조건을 미리 정하여 인덱스로 배열에 접근하기 때문에 빠르다.

2. for of 문
ES6에 도입된 반복문으로 배열또는 iterable 객체에서 **순차적**으로 요소를 가져오는 방식이다.   
for문보다 약간 느리지만 가독성이 좋다.

3. forEach 메서드   
forEach는 배열의 각 요소에 대한 콜백함수를 실행하는 메소드.   
콜백 함수 호출로 인한 오버헤드 때문에 for, for of 보다 성능이 떨어질 수 있다고 한다.

