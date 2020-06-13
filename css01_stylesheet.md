# css style

>css 기본 문법 작성방식에는 3가지가 있다
>
>- 인라인 스타일시트 : 인라인 시트는 태그에 바로 속성을 주어서 작성하며 우선순위가 가장 높다.
>
>  ```html
>  <b style="color : blue;">1. 인라인 스타일시트 : 우선순위가 높다.</b>
>  ```
>
>  
>
>- 내부 스타일시트 :  html 내부에 간단하게 작성하는 스타일시트이다.
>
>  ```html
>  <!DOCTYPE html>
>  <html>
>  <head>
>  <meta charset="UTF-8">
>  <title>Insert title here</title>
>  <style type="text/css">
>      p{
>          background-color : pink;
>      }
>      b{
>          background-color : gray;
>      }
>      h1{
>          background-color : blue;
>      }
>  </style>
>  </head>
>  <body>
>  	<h1>
>          css기본 문법
>      </h1>
>      <p>
>          <span>2. 내부 스타일시트 : html 내부에서 간단하게 작성</span>
>      </p>
>  </body>
>  </html>
>  ```
>
>  
>
>- 외부 스타일시트 : .css파일을 만들어서 그 안에 작성을 하고 불러온다.
>
>  ```html
>  <!-- WebContent/resources/css/basic.css -->
>  h3{
>  	color : red;
>  }
>  ```
>
>  ```html
>  <!DOCTYPE html>
>  <html>
>  <head>
>  <meta charset="UTF-8">
>  <title>Insert title here</title>
>  <style type="text/css">
>  	@importurl("resources/css/basic.css"); /*가지고오는, 불러오는 구문*/
>  </style>
>      <!-- 위의 방법으로 가져오거나 혹은 link를 써서 불러올 수 있다. -->
>      <!-- link href="resources/css/basic.css" rel="stylesheet" type="text/css"/> -->
>  </head>
>  <body>
>  	<h3>
>          작성방식 3가지
>      </h3>
>      <p>
>          <b>3. 외부 스타일시트 : .css파일을 만들어서 작성.</b>
>      </p>
>  </body>
>  </html>
>  ```

> 외부 스타일시트를 불러오는 방법은 2가지가 있는데 style type="text/css" 태그 안에
>
> @importurl("resources/css/basic.css"); 로 작성하는 방법과
>
> head 태그 안에 link href="resources/css/basic.css" rel="stylesheet" type="text/css"로 불러오는 방법이 있다.
>
> **href** 는 파일 경로를 뜻하고, **rel**은 연결 대상의 속성을 뜻하고, **type**는 해당 파일의 정보값을 의미한다.

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjM4/MDAxNTkyMDc4NzM2MzY3.soX-H6gRpJli5tbIYm1M3FWbbD6hbgIG0JrgKYUHkDQg.4twywNIIZWkCYRp4wrVbB5o-39J-Rd6Sjsx1aIDPKMkg.PNG.rgusqls/image.png?type=w773)



> css기본 문법 작성 결과화면이다.