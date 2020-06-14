# border

>border은 기본적으로 테두리를 입힐 때 사용하는 속성이다.
>
>border 속성 사용법은 [ border : 두께 선종류 색상] 으로 이루어져 있다.
>
>ex > border : 1px solid black
>
>border와 연관 되어있는 radius 속성을 같이 사용하는 예제를 알아보자.
>
>radius : 사각형의 border을 둥글게 만들어주는 속성이다.
>
>ex > border-radius : (top-left), (top-right), (bottom-right), (bottom-left); 순으로 작성한다.
>
>border-radius 속성을 줄 때는 브라우저마다 속성명령어가 다르다.
>
>- -webkit-border-radius : 구글, 사파리
>- -moz-border-radius : 파이어폭스
>- -ms-border-radius : 익스플로러
>- -o-border-radius : 오페라



```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<style type="text/css">
    *{
        padding : 0px;
        margin : 0px;
    }
    body{
        font : 30px "Arial Black";
        color : #333;
        margin : 20px;
    }
    li{
        list-style : none;
        width : 100px;
        height : 100px;
        text-align : center;
        float : left;
        border-radius : 50px 50px 50px 50px;
        box-shadow:inset 20px 30px 20px 1px raba(18,52,86,0.8);
    }
    .c1{background-color:red;}
    .c2{background-color:green;}
    .c3{background-color:blue;}
    .c4{background-color:pink;}
</style>
</head>
<body>
	<ul>
        <li class="c1">J</li>
        <li class="c2">A</li>
        <li class="c3">V</li>
        <li class="c4">A</li>
    </ul>
</body>
</html>
```

> 이 예제에서 처음 보는 속성 두 가지만 얘기하겠다.
>
> - list-style : none;
>
>   list인 ul,ol,dl 앞에 붙는 수식어를 제거해준다는 의미를 가진다.
>
> - box-shadow : inset 20px 30px 20px 1px raba(18,52,86,0.8);
>
>   box의 그림자를 지정해주는 속성이다.
>
>   raba 의 마지막a는 불투명도를 의미한다.
>
>   - none : 그림자 효과를 없앤다
>   - x-position : 가로 위치입니다. 양수면 오른쪽에, 음수면 왼쪽에 그림자가 만들어진다. (필수)
>   - y-position : 세로 위치입니다. 양수면 아래쪽에, 음수면 위쪽에 그림자가 만들어진다. (필수)
>   - blur : 그림자를 흐릿하게 만듭니다. 값이 클 수록 더욱 흐려진다.
>   - spread : 양수면 그림자를 확장하고, 음수면 축소한다.
>   - color : 그림자 색을 정한다.
>   - inset : 그림자를 요소의 안쪽에 만든다.

> + **중요한 사실 !**
>
>   word-wrap 속성은 자동으로 지정된 태그의 영역 안에 들어온다. 칸이 넘어가지 않도록 해주는 속성이다.

---------------

# transform

> css에 추가된 속성으로 변형을 해주는 속성이다.
>
> transform 속성에는 여러가지 속성이 있다.
>
> - **transform : translate(픽셀, 픽셀)**
>
>   위치 이동을 해주는 속성이고 x,y만큼 이동한다는 의미를 가진다.
>
>   ```html
>   <!DOCTYPE html>
>   <html>
>   <head>
>   <meta charset="UTF-8">
>   <title>Insert title here</title>
>   <style type="text/css">
>       #talate{
>           width : 200px;
>           height : 200px;
>           background : red;
>           color : white;
>           font-size:30pt;
>           word-wrap : break-word;
>           transform : translate(50px, 50px);
>       }
>   </style>
>   </head>
>   <body>
>   	<h1>Transform-translate</h1>
>       <div id = "tlate">translate(x, y) : 위치이동</div>
>   </body>
>   </html>
>   ```

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjI4/MDAxNTkyMTEyMTk4MTk4.o70Q-EViNJ7gNG6Z8r_JsAb47ZbRGOPx5cn7g7kZnbsg.OIXu2UQYGem0greE9LB8ZpI4ef4fqEzk4syvxQos-v4g.PNG.rgusqls/image.png?type=w773)



> - **transform : rotate(30deg);**
>
>   지정된 태그를 deg만큼 횐한다는 의미이다.
>
>   ```html
>   <!DOCTYPE html>
>   <html>
>   <head>
>   <meta charset="UTF-8">
>   <title>Insert title here</title>
>   <style type="text/css">
>       #troate{
>           width : 200px;
>           height : 200px; 
>           black-color : red;
>           font-size : 30pt;
>           word-wrap : break-word;
>           transform : rotate(30deg);
>           /*30deg만큼 회전시켜달라는 의미*/
>       }
>   </style>
>   </head>
>   <body>
>   	<h1>Transform-rotate</h1>
>       <div id = "trotate">rotate(deg) : 회전</div>
>   </body>
>   </html>
>   ```

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTUx/MDAxNTkyMTEyMjc4NTU3.Dw1MLQ6JXZBuFBVVzKQFaI7rzt7SFaYqUZgQEIp8IT0g.LRn2L--rDnr08eqUUOHkFoBZljBAsXrrHly_eYr0_v8g.PNG.rgusqls/image.png?type=w773)



> - **transform : scale(?,?);**
>
>   scale는 원래의 크기보다 ?% 작게 만들어달라는 의미다.
>
>   ex > transform : scale(0.6,0.6);
>
>   원래의 크기보다 60%작게 만들어달라는 의미.
>
>   ```html
>   <!DOCTYPE html>
>   <html>
>   <head>
>   <meta charset="UTF-8">
>   <title>Insert title here</title>
>   <style type="text/css">
>   #tscale {
>   	width : 200px;
>   	height : 200px;
>   	background-color : red;
>   	color : white;
>   	font-size : 30pt;
>   	word-wrap : break-word;
>   	transform : scale(0.6,0.6);
>   	/*원래 크기보다 60% 작게 만들어 달라는 의미.*/
>   }
>   </style>
>   </head>
>   <body>
>   	<h1>Transform - scale</h1>
>   	<div id="tscale">scale(x,y) : 크기</div>
>   </body>
>   </html>
>   ```

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjgz/MDAxNTkyMTEyMzI2OTA1.wi7i-8NXO2I57IyCrvWyi0eJLcWQVg8lN1H_mR9P3Rwg.3Ac6L_rkUpcG4wEcwqm-K9NvwG6yO_vDS1_xItKhvesg.PNG.rgusqls/image.png?type=w773)



>- **transform : skew(?deg, ?deg);**
>
>  skew는 기울기를 주는 속성이다.
>
>  첫번째 deg는 가로 기울기, 두번째 deg는 세로 
>
>  ex > transform : skew(20deg, 20deg);
>
>  ```html
>  <!DOCTYPE html>
>  <html>
>  <head>
>  <meta charset="UTF-8">
>  <title>Insert title here</title>
>  <style type="text/css">
>  #tskew{
>  	width : 200px;
>  	height : 200px;
>  	background-color : red;
>  	color : white;
>  	font-size : 30pt;
>  	word-wrap : break-word;
>  	transform : skew(0deg, 10deg);
>  }
>  </style>
>  </head>
>  <body>
>  	<h1>Transform - skew</h1>
>  	<div id="tskew">skew(deg,deg) : 모양을 변형</div>
>  </body>
>  </html>
>  ```

![](https://postfiles.pstatic.net/MjAyMDA2MTRfNSAg/MDAxNTkyMTEyMzczNjQx.z0bIDKthrRBELQHLRIs8Nody0-TIJIx759bZbHWhiF4g.s4hB_B_wmsSVu6iJFC4iraV5uscAugdPd8KJys9AdDog.PNG.rgusqls/image.png?type=w773)



>- transform 중에 transition을 사용한 서서히 변환시키기.
>
>  속성들을 변환시켜주는 기능을 가진 속성이다.
>
>  ex > transition : width 0.5s, background : 1.5s, linear, transfrom 1.5s;
>
>  width를 0.5초만에 background를 1.5초만에, 부드럽게, transform을 1.5초만에 변환시켜준다.
>
>  ```html
>  <!DOCTYPE html>
>  <html>
>  <head>
>  <meta charset="UTF-8">
>  <title>Insert title here</title>
>  <style type="text/css">
>  #tran{
>  	width : 200px;
>  	height: 200px;
>  	background-color: red;
>  	color : white;
>  	font-size : 30pt;
>  	word-wrap : break-word;
>  	transition : width 0.5s, background 1.5s linear, transform 1.5s;
>  }
>  #tran:hover{
>  	width : 800px;
>  	background-color: blue;
>  	transform : translate(300px,0px);
>  }
>  </style>
>  </head>
>  <body>
>  	<h1>Transform 속성 전환</h1>
>  	<div id="tran">transition</div>
>  </body>
>  </html>
>  ```
>
>  위와 같이 transition 속성을 준 후 밑에 #trans:hover이라는 의미는 
>
>  id가 trans라는 태그 문구에 마우스를 올리면 width는 800px, 배경은 blue, translate(위치변경)
>
>  을 실행해주는데 transition이 저 기능들을 가지고 변환시켜준다.

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjYy/MDAxNTkyMTEyNDM1OTI4.nB3I9wK9r0XN20rBC2XxsKGwj3ELbBKSd2WVLg0NZUIg.12QAPWp6NBfF7ii2cJrUy25wTc_4zl6BEMtjE8Drj0Ag.PNG.rgusqls/image.png?type=w773)



> - transition을 이용한 메뉴바 이쁘게 꾸미기.
>
>   ```html
>   <!DOCTYPE html>
>   <html>
>   <head>
>   <meta charset="UTF-8">
>   <title>Insert title here</title>
>   <style type="text/css">
>      li{
>         width: 500px;
>         background: grey;
>         margin-bottom: 3px;
>         font-size: 30pt;
>         font-weight: bold;
>         list-style-type: none;
>         cursor: pointer;
>         transition: width 1s linear, color 1s linear, letter-spacing 1s;
>      }
>      li:hover{
>         width : 800px;
>         color: red;
>         letter-spacing: 5px;
>      }
>   </style>
>   </head>
>   <body>
>   	<div>
>   		<h1>Main menu</h1>
>   			<ul>
>   				<li>COMPANY</li>
>   				<li>PRODUCT</li>
>   				<li>SERVICE</li>
>   				<li>COMMUNITY</li>
>   			</ul>
>   	</div>
>   </body>
>   </html>
>   ```
>
>   li 태그에 적힌 문구에 마우스를 올리면 width를 800px, color은 red, letter-spacing(글자간 공백 넓이) : 5px 로 변형시켜준다.
>
>   이 때 transition속성을 width 1s, linear, color 1s linear, letter-spacing 1s;로 주어서
>
>   이쁘게 꾸며주었다.
>
>   ![](https://postfiles.pstatic.net/MjAyMDA2MTRfOTYg/MDAxNTkyMTEyNDk0NTYy.R_N7KtWFKFj80Asw4H4D8yKK-WMcTLm9jMkN9RecEpkg.Pn54vrdPtFwgMITJA43OK-A6QQaw67VKuSlcXUaeg1og.PNG.rgusqls/image.png?type=w773)



