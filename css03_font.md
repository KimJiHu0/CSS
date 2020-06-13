# css03 font

> 폰트를 적용시키는 속성은 여러가지가 있다.
>
> font-weight : 글씨를 굵게 만들어준다.
>
> font-style : 글씨의 모양을 바꿔준다.
>
> - normal : 보통 모양입니다.
> - italic : 기울임꼴입니다.
> - oblique : 기울임꼴입니다.
> - initial : 기본값으로 설정합니다.
> - inherit : 부모 요소의 속성값을 상속받습니다.
>
> font-variant : 소문자를 대문자로 만드는데, 일반 대문자 크기에 비해 더 작다.
>
> font-size : 폰트의 크기를 지정한다.
>
> line-height : 줄간격을 의미한다.
>
> font-family : 글씨체를 지정해준다.

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>css03</title>

<style type="text/css">


div h1{
font-weight: bold;
font-style:italic;
font-variant: small-caps;

font-size:25px;
line-height:500%;

font-family:"궁서";
}

div h1 {
	font: bold italic small-caps 25px/500% "궁서";
}
</style>

</head>
<body>

	<div>
		<h1>BigData 전문가 과정 : 4월 15일 개강</h1>
	</div>

	<h1>BigData 전문가 과정 : 4월 15일 개강</h1>

</body>
</html>
```

![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjU4/MDAxNTkyMDgxMDYyNzQ1.sKvGBqryvWTRAiOQKU4auNc1ZLp16tUIHLZqTmgGojwg.ptTSbcE7u31GcbcMyIZu2ryMxlYz-O5EDdSxzD6xHcgg.PNG.rgusqls/image.png?type=w773)