# overflow



![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTA5/MDAxNTkyMDg2OTQ4Mzk1.VedmGBQd5sIqqm3QKbK-ppA4NafLKO0vQxv17_07kw0g.9vILb0ciOoiB8mQ5BjvNKwVpTjuW9ZOyFL64FtljOIsg.PNG.rgusqls/image.png?type=w773)

> overflow : hidden; 을 한 실행 결과
>
> 태그에 넘치는 부분들을 숨겨준다



![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTMw/MDAxNTkyMDg3MDE2Mjgx.WTJ-BGHJZQLeND-34T8gm-_E2AtAk1qlX1HIUrRk5fgg.kWMPAXbfqa9yTRYTGXmgRjNvc73t-_ZFku1gmzQyTesg.PNG.rgusqls/image.png?type=w773)

> overflow : auto; 를 한 실행 결과
>
> width를 자동으로 잡아주어 좌우스크롤이 없고 상하 스크롤만 있다.



![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTU3/MDAxNTkyMDg3MDk4NjA5.avX-BJ7o0hhB32U7RLgpcP3KA6z6epfc38WhtpK4vw0g.PYbjHDFjxgKEsxuakohId-K1nTblHDJXGilhgIDH-8wg.PNG.rgusqls/image.png?type=w773)

> overflow : scroll; 을 한 실행 결과
>
> 좌우스크롤과 상하스크롤이 생긴다.

---------------

# position

>position은 웹 문서 안 요소들을 어떻게 어디에 배치할지 정하는 속성이다.
>
>- position : relative
>
>  원래의 위치에서 얼만큼 움직이는지 볼 수 있다.
>
>- position : absolute
>
>  부모의 위치에서 상대적으로 얼만큼 움직이는지 볼 수 있다.
>
>- position : fixed
>
>  브라우저 스크롤이 움직여도 고정시킨다.



```html
<style type="text/css">
	#box {
	border: 1px solid black;
	width : 550px;
}

.myred {
	background: red;
	position : relative;
}

.myblue {
	background: blue;
	position : absolute;
	left : 100px;
	top : 30px;
	z-index: 2;
}

.mygreen {
	background: green;
	position : relative;
	left : 20px;
	bottom : 30px;
}

p {
	width: 130px;
	height: 80px;
	color: #fff;
	font-weight: bold;
}
.myred:hover{z-index:100;}
.myblue:hover{z-index:100;}
.mygreen:hover{z-index:100}
#fixed{
		width:100px;
		height:300px;
		background-color:silver;
		position:fixed;
		right:50px;
		top:100px;
		}
</style>
<body>
    <div id="box">
        <p class="myred">박스의 크기와 위치를 잘 생각해보자</p>
        <p class="myblue">박스와 포지션 속성을 바꿔가며 테스트해보자</p>
        <p class="mygreen">포지션은 많이 사용해봐야한다.</p>
    </div>
    
    <div id="fixed">
       	Fixed!!
    </div>
</body>
```

> .myblue의 position 속성은 **absolute**이다.
>
> .myblue의 부모인 #box의 위치에서부터 left, top를 주었다.
>
> **z-index**는 3차원 도형으로 보왔을때 입체감을 의미한다.
>
> 즉, z-index가 클수록 앞으로 나온다는 의미다.
>
> .mygreen은 **relative**라는 속성을 주었다. 이는 .mygreen의 위치에서 left와 bottom을 주었다.
>
> #fixed는 위치를 고정시킨다는 속성이다.
>
> 브라우저의 길이가 길어서 스크롤을 밑으로 내려도 **fixed** 속성인 태그는 그대로 고정되어있다.
>
> **:hover** 은 ~위에 마우스를 올렸을 때 일어나는 현상을 의미한다.
>
> 현재 .myblue의 z-index가 가장 크기 때문에 가장 앞에 나와있는데, 호버를 하면 다른 창이 z-index가 100이 되기 때문에 가장 앞에 있을 것이다.



![](https://postfiles.pstatic.net/MjAyMDA2MTRfOTYg/MDAxNTkyMDg3MzQwMDAx.ypvGslLsH8T4Sj-EcQX3PdNu-CaARDVmRFcluMS2X_sg.tGDDDb9dma-uh-JSsP1v-ylCTfkBy9197TXQ_-Dd648g.PNG.rgusqls/image.png?type=w773)

