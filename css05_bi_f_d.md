# background img

> - **background-image :** url("") 에 파일 경로를 입력하여 배경에 이미지를 깔아준다.
>
> - **background-repeat :** 반복해서 사용할건지 지정해주는 속성.
>
>   repeat : 가로 방향, 세로 방향으로 반복합니다.
>
>   repeat-x : 가로 방향으로 반복합니다.
>
>   repeat-y : 세로 방향으로 반복합니다.
>
>   no-repeat : 반복하지 않습니다.
>
> - **background-attachment :** 사진을 움직일건지 지정해주는 속성.
>
>   scroll : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지는 스크롤되지 않습니다.
>
>   fixed : 움직이지 않습니다.
>
>   local : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지도 스크롤됩니다.
>
> - **background position :** 배경 이미지의 위치를 지정해주는 속성.
>
>   left , right : 가로의 좌, 우 위치를 지정해준다.
>
>   top, bottom : 세로의 위, 아래 위치를 지정해준다.



----------------------------------------------------------------------------------------------------------------------------------------------------

# float

>float의 정의는 특정 요소를 떠있게, 흐르도록, 부유하게 하도록 하는 속성
>
>말로하기 힘들기 때문에 사진을 첨부하겠다.



- **float 속성을 주지 않았을 때**

![](https://postfiles.pstatic.net/MjAyMDA2MTRfOTkg/MDAxNTkyMDgzNjM3MjA2.Aj_UBIqNc2h5QCV2yO2cRSnaGpHjs0q2pkbAopR5f5Ig.A0RoUBNxIf4tB-I9L_EGc_n1I-PE5nCMaDzY7XnN1Jog.PNG.rgusqls/image.png?type=w773)

>p태그의 속성으로 줄바꿈이 자동으로 되었으며, 자신의 영역을 가지고 있다.



- **float 속성을 left로 주었을 때**

![](https://postfiles.pstatic.net/MjAyMDA2MTRfODAg/MDAxNTkyMDgzNzA1MjE1.OnTr3sQny_IkqI5W_BM685B-QgXtGdx5dJGrq_BNEzYg.FLE6TLJ6vy2x7hRc4rzDklXF2h3dnF9mb9O2VqkSV90g.PNG.rgusqls/image.png?type=w773)

> p태그의 속성을 무시하고 자신의 텍스트 크기만큼의 영역이 되었고, 왼쪽으로 밀착하게 되었다.
>
> ```html
> <!-- 내부스타일 시트로 float를 주겠다. -->
> p{
> 	float : left; <!-- 왼쪽 모서리로 밀착하게 된다. -->
> 	float : right; <!-- 오른쪽 모서리로 밀착하게 된다. -->
> 	clear : both; <!-- 만약 다른 태그의 속성으로 float속성을 주었고 또 다른 태그에 clear : both 속성을 주었을 때 float 속성들을 모두 없애주는 속성이다. -->
> }
> ```
>
> 

---------------------------

# display

> display 속성은 요소의 종류를 선택하는 속성이다.
>
> 원래 inline요소를 block 요소로 보이게 만들 수 있고,
>
> 원래 block요소를 inline요소로 보이게 만들수도 있다.



![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTcx/MDAxNTkyMDg1Nzc1NDQ2.0P6rocxPy_G4_UL6OyWzWxHYTzpbo8wJO0a4E01DQh0g.T12P-ZhT6XW2N8kYf0gy-DmYioN2Mj2HcLkD1p0468Ug.PNG.rgusqls/image.png?type=w773)

> div를 활용해 출력한 것이다. 아래의 속성들을 하나씩 줘보겠다.



- **display : inline**

  기본값으로 요소를 inline 요소처럼 표시한다.

  따라서 앞뒤로 줄바꿈이 되지 않는다.

  ![](https://postfiles.pstatic.net/MjAyMDA2MTRfMjkg/MDAxNTkyMDg1ODY1NTg3.Ylg5hhq-dISmEk3KUyJWUOjQ5qJ7kyhSMfh3_8TdLh4g.FYz68UPtmF483Z2v8788WMcMN4ykOcNSFf8TPsvwTQ8g.PNG.rgusqls/image.png?type=w773)

- **display : block**

  요소를 block 요소처럼 표시한다.

  따라서 요소 앞 뒤로 줄바꿈이 된다.

  >span 태그로 위의 그림처럼 만든 후 display : block를 하게 되면 맨 처음 만들었던 그 결과가 나온다.

- **display : none**

  박스가 생성되지 않는다.

  따라서 공간을 차지하지도 않는다.

  > display:none 를 하게 되면 이 속성을 준 태그들은 화면에 보여지지 않게 된다.

- **display : inline-block**

  요소는 inline요소인데 내부는 block 요소처럼 표시한다.

  즉, 박스 모양이 inline처럼 옆으로 늘어선다.

  ![](https://postfiles.pstatic.net/MjAyMDA2MTRfMTc4/MDAxNTkyMDg2MTgyMjQx.x4TB_lxkCu7xditjBVP25NLBpR1qUVn7cs_zRs_qQ_Ag.ga4nZabsuu_f2_JzzDJWZkmvVPzovivWBgPpxCisEFQg.PNG.rgusqls/image.png?type=w773)

> 원래 인라인요소는 자신이 가진 텍스트의 크기만큼만 크기가 지정되어 있어서 width, height 속성이 적용되지 않는다. 그렇지만 display : inline-block; 를 해주게 되면 인라인요소인데 내부만 블록요소처럼 표시해서 width속성과 height 속성이 적용되지만 인라인요소이기 때문에 가로로 늘어선다.