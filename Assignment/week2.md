# Week 2 
## What is Alpha and Digital color?

### Alpha

#### Alpha compositing

알파 합성은 하나의 이미지를 배경과 결합하여 부분적으로나 전체를 투명하게 만드는 과정이다.

#### Who founded this?

알파 합성의 개념은 1970년대 말 앨비 레이 스미스(Alvy Ray Smith)가 처음 선보였고 1984년에 토머스 포터(Thomas Porter)와 톰 더프(Tom Duff)에 의해 백서를 통해 완전히 개발되었다

### Color
색의 3속성
- 색상(Hue): 색을 구별하는 속성
- 명도(Saturation): 색의 밝고 어두운 정도, 색의 밝기
- 채도(Value): 색의 강약과 선명한 정도


### Digital Color
디지털 신호에 의해 만들어진 색채 표현방법, 최소의 단위는 비트(Bit), 디지털 이미지의 최소 단위는 화소(픽셀 Pixel).

비트가 모여 화소(픽셀 Pixel)를 나타내며 화소는 이미지의 선명도와 질선명도를 결정짓는 요소로 픽셀 수에 의해 차이가 발생한다.

### Digital Color Mode

#### RGB(Red, Green, Blue)

: 빛을 이용한 표시 장치에 사용되는 컬러

빨간색(Red), 녹색(Green), 파란색(Blue)의 혼합으로 이루어진다. 혼합할수록 색이 밝아진다

- 가산혼합(additive color mixing): 빛을 가하여 색을 혼합할때 혼합한 색이 원래의 색보다 밝아지는 혼합

![alt text](https://upload.wikimedia.org/wikipedia/commons/7/7b/AdditiveColorMixingII.png)

확대하면, 모니터의 색상이 3가지 색상으로 표시된다.

![alt text](https://designmanagementlucerne.files.wordpress.com/2013/10/28.png)

빨간색, 녹색, 파란색 세 가지의 조합으로 만들어진 화소는 바이트를 이용하여 각각 빨간색 1바이트, 초록색 1바이트, 파란색 1바이트가 들어간다.
1바이트는 0부터 255까지 총 256단계의 색을 나타낼 수 있다.

RGB (255,0,0)= 빨간색,
RGB (255,100,0)= 초록색이 섞인 연한 빨간색

특징: 색 표현력이 높아 있는 그대로의 색을 재현한다.

#### CMYK(Cyan, Magenta, Yellow, Key=Black)
: 인쇄용 컬러

시안(Cyan), 마젠타(Magenta), 옐로(Yellow)의 혼합과 키(Key)컬러 블랙의 추가로 표현된다. 혼합할수록 색이 어두워진다.

- 감산혼합(subtractive color mixing): 혼합한 색이 원래의 색보다 명도가 낮아지도록 색을 혼합하는 방법

![alt text](https://upload.wikimedia.org/wikipedia/commons/2/24/SubtractiveColorMixingII.png)

확대하면, 4가지의 색상으로 이루어져 있다

![alt text](https://designmanagementlucerne.files.wordpress.com/2013/10/30.png)

색 표현력이 제한적이라 RGB보다 풍부한 색 표현이 불가능하다.
