# SystemPrograming
Markdown practice 
===========================
1.마크다운이란? 
----------------------
> Markdown은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 
만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 
특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 
웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 
----------------------
1.1 마크다운의 장-단점
-------------------
1.1.1 장점 
> 1. 간결하다. 
> 2. 별도의 도구없이 작성가능하다.
> 3. 다양한 형태로 변환이 가능하다. 
> 4. 텍스트로 저장되기 때문에 용량이 적어 보관이 용이하다.
> 5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리 할 수 있다.
> 6. 지원하는 프로그램과 플랫폼이 다양하다.
------------------------
1.1.2 단점
> 1. 표준이 없다.
> 2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다. 
> 3. 모든 HTML 마크업을 대신하지 못한다.
=================

2 마크다운 사용법  
-------------------
2.1 헤더 Headers 
 * 큰제목 : 문서 제목 
    > This is an H1 아랫줄에 ======= 2단줄 해주면 큰제목으로 변경된다. 

 * 작은제목 : 문서 부제목 
    > This is an H2 아랫줄에 ------- 1단줄 해주면 부제목으로 
    변경된다.

 * 글머리 1~6까지만 지원
 >  
    # This is a H1 
    ## This is a H2 
    ### This is a H3 
    #### This is a H4
    ##### This is a H5
    ###### This is a H6 
 > # This is a H1 
 >> ## This is a H2 
 >>> ### This is a H3 
 >>>> #### This is a H4 
 >>>>> ##### This is a H5 
 >>>>>> ###### This is a H6 
---------------------------

2.2 BlockQuote 
------------------------
이메일에서 사용하는 > 블럭인용문자를 이용한다. 

> This is a first blockqute.   
    첫번째 문단 
> > This is a second blockqute.

>>> This is a third blockqute. 

-------------
2.3 목록
-----------------
 * 순서있는 목록(번호):
 
    순서있는 목록은 숫자와 점을 사용한다. 
    > 1. 첫번째
    > 2. 두번째
    > 3. 세번째 

    *현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다. *

 * 순서없는 목록(글머리 기호 *,+,- 지원)
 >
     *빨강 
        *녹색
            *파랑  
    
    +빨강 
        +녹색
            +파랑

    -빨강
        -녹색
            -파랑 

* 빨강
    * 녹색 
        * 파랑 

혼합해서 사용하는 것도 가능하다.
>
    * 1단계 
        - 2단계
            + 3단계
                + 4단계

* 1단계 
     - 2단계
        + 3단계
            + 4단계 

-------------------------------
2.4 코드 
--------------------
2.4.1 들여쓰기
> 
This is a normal paragraph : 

    This is a code block.
end code block.

한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생한다.
>
     This is a normal paragraph:
        this is a code block.
    end code block.

적용예 :

    This is a normal paragraph: This is a code block. end code block. 
-------------------------
2.4.1 **코드블럭**   
코드블럭은 다음과 같이 2가지 방식을 사용할 수 있다.   
    
* > 
    <테스트 pre><테스트 code>{code}</테스트 code></테스트 pre> 이용방식 

<pre>
<code>
public class TestApplication {
    public static void main(String[] args){
        System.out.Println ("Hello, Minwoo");
    }
}
</code>
</pre>

* 코드블럭코드 ("```")을 이용하는 방법 

``` 
```public class TestApplication{
    public static void main(String[] args){
        System.out.println("Hello, Minwoo");
    }
} ```
```

**깃헙** 에서는 코드블럭코드("```") 시작점에 사용하는 언어를 선언하여 문법강조 (Syntax highlighting)이 가능하다.
 

 ```java 
 public class TestApplication{
         public static void main(String[] args){
        System.out.println("Hello, Minwoo");
    }
} ```
}
```

```java 
public class TestApplication{
         public static void main(String[] args){
        System.out.println("Hello, Minwoo");
    }
}
```
- - -
2.5 수평선 <hr/>
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용한다.
 >
    * * *
    ***
    *****
    - - -
    ----------------------

* 적용예 
* * *
- - - 
******* 
-------------------

2.6 링크
- - - 
* 참조링크 
> 
    [link keyword][id]
    [id] : URL " Some Title here"

    //code 
    Link: [Google][googlelink]

    [googlelink]: https://google.come "Go google"

Link: [Google][http://google.com] 

* 외부링크 
>
    사용문법: [Title](link)
    적용예: [Google](https://google.com. "google link")

Link : [Google](https://google.com)
 
* 자동연결
>
    일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.
    * 외부링크 : <http://example.com>
    * 이메일링크 : <example@example.com>
* 외부링크: <http://google.com>
* 이메일링크: <address@example.com>

2.7 강조 
- - -
>
    *single asterisks*
    _single underscores_
    **double asterisks**
    __dobule underscores__
    ~~cancelline~~ 

*yes or no*   

_yes or no_

**yes or no**

__yes or no__

~~yes or no~~ 

2.8 **이미지**
- - -
> 
    ![Alt text](/path/to/img.jsp)
    ![Alt text](/path/to/img.jpg "Optional title")

![testPhoto](/images/testPhoto.jpg)

사이즈 조절 기능은 없기 때문에 
> 
    <img width="" height=""></img>
를 이용한다.

# *참고문서

* [마크다운 사용법 제공 ](https://gist.github.com/ihoneymon/652be052a0727ad59601)
