# animation

> - #### css속성 animation 과 keyframes
>
>   keyframesa는 animation이 시작부터 끝까지 어떤 동작을 할것인지 지정하는 css문법이다.
>
>   
>
>   ```html
>   	div{
>   		width:100px;
>   		height: 100px;
>   		font-size : 30pt;
>   		background-color: red;
>   		animation : mybox 2s infinite;
>   	}
>   ```
>
>   css부분은 위와 같이 작성했다.
>
>   animation 속성 부분은 my박스를 2초에 한번씩 바뀌게 하였고 무한반복하게 만든 구문이다.
>
>   
>
>   ```html
>   	@keyframes mybox{
>   		0%{width : 150px; height : 150px; background:yellow; transform:translate(10px,10px);}
>   		25%{width : 200px; height : 200px; background:blue; transform:translate(50px,50px);}
>   		50%{width : 250px; height : 250px; background:orange; transform:translate(100px,100px);}
>   		75%{width : 300px; height : 300px; background:pink; transform:translate(50px,50px);}
>   		100%{width : 200px; height : 200px; background:red; transform:translate(10px,10px);}
>   	}
>   ```
>
>   위의 예제처럼 사용할 수 있는데 0%는 animation  효과의 시작을 의미하고 100%는 끝을 의미한다.
>
>   위처럼 5번의 나눔 뿐만 아니라 더 부드럽게 만들고 싶다면 저 많이 쪼갤 수 있다.
>
>   그럼 이제 이미지는 2초에 한번 바뀌는데 5번으로 나눠서 변해진다.
>
> -------------------



# multi ui

mulit_ui가 쓰이는 속성은 colmun-count, column-gap, column-rule를 사용하였다

```html
	p{
		column-count:3;
		column-gap:20px;
		column-rule:2px solid red;
	}
```

> column 이란 table에서도 그렇고 DataBase도 그렇고 컬럼은 세로를 의미한다.
>
> 해석하고 보면 세로의 갯수를 3개로, 컬럼간의 간격을 20px, 컬럼들끼리 빨간 실선으로 경계를 두었다.