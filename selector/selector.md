# 선택자(Selector)


## 연결 선택자

* 하위 선택자(descendant selector)

    * section p {...}
    * section 태그 하위 모든 p
    
    ```
    <style>

    section p {color:red}

    </style>

    <section>

    <p>lorem ipsum</p><!--// 색상 적용 O -->

    <div>
        <p>lorem ipsum</p> <!--// 색상 적용 O -->
    </div>

    </section>

    ```



* 자식 선택자(child selector)
    * section > p {...}
    * 하위 선택자와는 다르게 자식까지만 적용(손자x)
    
    ```
    <style>

    section p {color:red}

    </style>

    <section>

    <p>lorem ipsum</p><!--// 색상 적용 O-->

    <div>
        <p>lorem ipsum</p> <!--// 색상 적용 X -->
    </div>

    </section>

    ```



* 인접형제 선택자
    * h2 + p {...}
    * h2의 인접한 형제 첫 번째 p만

    ```
    <style>

    h2 + p {color:red}

    </style>

    <section>
    <h2> head 2</h2>
    <p>lorem ipsum</p><!--// 여기만 색상 적용 O -->
    <p>lorem ipsum</p><!--//  색상 적용 X -->
    <p>lorem ipsum</p><!--//  색상 적용 X -->

    </section>

    ```

* 형제 선택자
    * h2 ~ p {...}
    * h2의 형제 모든 p
    ```
    <style>

    h2 ~ p {color:red}

    </style>

    <section>
    <h2> head 2</h2>
    <p>lorem ipsum</p><!--// 색상 적용 O-->
    <p>lorem ipsum</p><!--// 색상 적용 O-->
    <p>lorem ipsum</p><!--// 색상 적용 O-->

    </section>

    ```  
  
## 속성 선택자

* [속성] 선택자

    * 특정 속성이 있는 요소를 선택

    ```
    a[href] {...}
    ```



* [속성 = 속성값] 선택자

    * 특정 속성값이 있는 요소를 선택 

    ```
    a[target=_blank] {...}
    ```


* [속성 ~= 속성값] 선택자

    * 정확하게 일치하는 요소만 선택
    * 


    ```
    <style>
    [class ~= btn] {...}
    </style>

    <div class="my-btn"></div>
    <div class="btns"></div>
    <div class="btn"></div><!--// 적용 O-->
    <div class="tmp btn"></div><!--// 적용 O-->
    ```


* [속성 |= 속성값] 선택자

    * 속성값이 포함된 요소를 선택
    
    * my-name 이라는 class에 my만 찾는 것이 아니라  
    my- 하이픈도 가능

    
* [속성 ^= 속성값] 선택자

    * 속성값으로 시작하는 요소 선택
    * value%

* [속성 $= 속성값] 선택자

    * 속성값으로 끝나는 요소 선택
    * ex) 확장자를 찾을 때 사용

    * %value

    ```
    [href=xls] {...}
    [src=jpg] {...}
    [src=png] {...}
    ```


* [속성 *= 속성값] 선택자

    * 속성값이 포함되어 있는 요소 선택(부분 검색)
    
    * %value%
    ```
    [href=naver] {...}
    ```



  
    

## 속성선택자 정리 

<table>
<tr>
<th>선택자<td>
<th>선택요소</th>
<th>CSS</th>
</tr>

<tr>
<td>[속성] 선택자<td>
<td>특정 속성이 있는 요소를 선택</td>
<td>href, require, etc...</td>
</tr>

<tr>
<td>[속성 = 속성값] 선택자<td>
<td></td>
<td></td>
</tr>


<tr>
<td><td>
<td></td>
<td></td>
</tr>

<tr>
<td><td>
<td></td>
<td></td>
</tr>

<tr>
<td><td>
<td></td>
<td></td>
</tr>

<tr>
<td><td>
<td></td>
<td></td>
</tr>

<tr>
<td><td>
<td></td>
<td></td>
</tr>



</table>




