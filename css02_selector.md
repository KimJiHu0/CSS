# css02 selector

> scc 선택자의 종류에는 여러가지가 있다.
>
> 선택자들을 사용하는 방법만 간다한게하고 설명하고 html문서에 주석으로 설명을 달아놓도록 하겠다.
>
> **타입 선택자 :** 태그의 이름을 불러와서 사용한다. [p{} h1{}]
>
> **id선택자 :** #을 사용하여 불러온다. [#sid01{} #sid02{}]
>
> **class 선택자 :** .을 사용하여 불러온다.  [.scls{}]
>
> **전체 선택자 :** *을 사용하여 불러온다. *{}
>
> **자식 선택자 :** >를 사용하여 불러온다. [#at > p{}]     id가at인 태그 밑에 p태그를 의미한다.
>
> ​                      #at > div > p ( id가 at인 태그 밑에 div태그 밑에 p를 의미한다.)
>
> **하위 선택자 :** 띄어쓰기를 사용하여 불러온다. div span{} ( div태그 아래 span태그)
>
> **인접 선택자 :** +를 사용하여 불러온다. [h3 + b{} ] h3태그에 인접한 b태그를 의미한다.
>
> **속성 선택자 :** []를 사용하여 불러온다. p[title] 는 title이 지정되어있는 모든 p태그를 의미하고 			  
>
> ​						p[title="b"] 는 title가 b인 p태그를 의미한다.
>
> **가상 클래스 선택자 :** [ :을 사용하여 불러온다. ] 가상클래스 선택자에는 여러가지고 있는데,
>
> ​									link : 링크의 속성을 정해주고, visited : 방문한 사이트의 속성을 정해주고,
>
> ​									hover : 마우스를 올렸을 때의 속성을 정해주고
>
> ​									checked : 체크를 했을 때 일어나는 속성을 정해준다.
>
> **종속 선택자 :** 타입선택자와 id선택자, class선택자가 혼합되어있는 선택자이다.
>
> **그룹 선택자 : **,로 여러 태그들을 한번에 언습하고 속성을 줄 수 있다. p,pre,strong{} 로 사용한다.

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<style type="text/css">
	/*타입 선택자.*/

pre{
	text-align:center;
}
h1{
	text-align: right;
	color:blue;
}

/*id 선택자*/

#sid01{
	color : purple;
}
#sid02{
	color : yellowgreen;
}
#sid03 {
	color : hotpink;
}

/*class 선택자*/
.scls{
	background-color : yellow;
}

/*전체 선택자*/
*{
	/*text-align : right;*/
}

/*자식 선택자*/
/*#at 바로 밑에있는 p태그 ( > 의미 )*/
#at > p {
	color : gold;	
}
#at > div > p {
	color : silver;
}

/*하위 선택자*/
div span{
	background-color : lime;
}

/*인접 선택자*/
h3 + b{
	color : navy;
}
b+span {
	background-color : black;
	color : white;
}

/*속성 선택자*/
p[title] {
	color : orange;
}
p[title="b"] {
	background-color:gray;
}

/*가상 클래스 선택자*/
a:link{
	color : green;
	font-size:25pt;
}
a:visited {
	color : red;
	font-size:15pt;
}
a:hover{
	background-color : fuchsia;
	font-family: fantasy;
	font-size:35pt;
	color : blue;
}
input:checked{
	width:100px;
	height:100px;
}

/*종속 선택자*/

li.scls01 {
	background-color : green;
}
li.scls02#sidul{
	font-size : 20pt;
}

/*그룹 선택자*/
p,pre,strong{
	color:#18cdff;
}
</style>
</head>
<body>
    
    	<h1>선택자.</h1>
	
	<article>
		<h3>타입 선택자</h3>
		<pre>태그 이름을 지정하여 선언</pre>
	</article>
	
	<article>
		<h3>id 선택자</h3>
			<ul>
				<li id = "sid01">요소에 id를 지정하고</li>
				<li id = "sid02">style에서 지정된 id값으로 사용</li>
				<li id = "sid03">#으로 구분한다.</li>			
			</ul>
	</article>
	
	<article>
		<h3>class 선택자</h3>
		<ol>
			<li class = "scls">요소에 class를 지정하고</li>
			<li class = "scls">style에서 지정된 class값으로 사용</li>
			<li class = "scls">.(dot)로 구분한다.</li>
		</ol>
	</article>
	
	<article>
		<h3>전체 선택자</h3>
	</article>
	
	<article id = "at">
		<h3>자식 선택자</h3>
		<div>
			<p>자식 1</p>
		</div>
		<p>자식 ?</p>
	</article>
	
	<article>
		<h3>하위 선택자</h3>
		<div>
			<span>특정 요소 하위의</span>
			<p>
				<span>요소를 지정할 떄 사용</span>
			</p>
		</div>
	</article>
	
	<article>
		<h3>인접 선택자</h3>
		<b>지정한 요소 다음</b>
		<span>에 나오는 요소 선택</span>
		<b>인접 ?</b>
	</article>
	
	<article>
		<h3>속성 선택자</h3>
		<p title = "a">속성이 정의된</p>
		<p title = "b">태그만 선택하는</p>
		<p>선택자!!</p>
	</article>
	
	<article>
		<h3>가상 클래스 선택자</h3>
		<ul>
			<li>특정 이벤트가 발생한 태그 선택!</li>
			<li><a href="http://www.naver.com">naver</li>
			<li><a href="http://www.google.com">google</a></li>
			<li><input type="checkbox"/>체크하면 효과적용</li>
		</ul>
	</article>
	
	<article>
		<h3>종속 선택자</h3>
		<ul>
			<li class="scls01">타입선택자와</li>
			<li class="scls02">id선택자(#)</li>
			<li class="scls01">class 선택자(.)</li>
			<li class="scls02" id="sidul">가 혼합된 형태입니다.</li>
		</ul>
	</article>
	
	<article>
		<h3>그룹 선택자</h3>
		<p>여러 요소에</p>
		<pre>각각 같은 속성을</pre>
		<strong>적용한다.</strong>
	</article>

</body>
</html>
```

