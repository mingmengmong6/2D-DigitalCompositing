# Week 2 
## What is Digital Compositing?

### Digital compositiong

연속된 이미지를 모아 디지털로 최종 이미지를 합성하는 과정으로, 일반적으로 인쇄, 동영상 또는 화면 디스플레이를 위해 사용된다. 디지털 컴포지팅에 사용되는 기본 연산을 '알파 블렌딩'이라고 한다.

#### Techniques

- Live action(실사 촬영)
- Blue or Green screen(블루/그린스크린)
- Rotoscoping(로토스코핑)
:애니메이션 이미지와 실사 동화상(live action) 이미지를 합성시키는 기법
- 2D or 3D images
- Particle Effects(파티클 이펙트)
- Matte Painting(매트 페인팅)
- Motion Capture(모션 캡쳐)
- Digital Actor(디지털 배우)
- Morphing(몰핑)

#### Layer-based vs. Node-based compositing

디지털 컴포지팅에는 바로 레이어 기반과 노드 기반 컴포지팅의 2가지 Work flow(워크플로우)가 있다. 노드기반이 더 시간이 절약되며, 더 사실적인 3D 공간을 다룬다.

| Layer-based      | Node-based       |
| ---------------- | -----------      | 
| comlicated       | more complicated |
| 3d place         | Real 3d space    |

#### Layer-based compositing

complicated compositing

|stacking order|
| ------------ |
|layer1        |
|layer2        |
|layer3        |
|layer4        |
|layer5        |

-> 오래된 작업순으로 레이어를 쌓아간다.
 빠른 2D 및 모션 그래픽과 같은 제한된 3D 효과에 적합하지만, 많고 복잡한 레이어을 갖는 컴포지트에는 어색해진다.
 
ex) After Effects

#### Node-based 

more complicated compositing

미디어 개체를 맵에서 연결한다. 이전 이미지 처리단계인 "context"의 파라미터를 수정할 수 있는 기능을 포함한 매우 유동적인 방법이다. 하지만 워크플로우는 레이어 기반 컴포지팅과 달리 타임라인에서 직접적으로 연결되지 않기 때문에 종종 키프레밍과 시간 효과를 제대로 처리하지 못하는 문제가 발생한다.

ex) Nuke, Fusion



## What is Alpha and Digital color?

### Alpha

#### Alpha compositing

알파 컴포지팅은 하나의 이미지를 배경과 결합하여 부분적으로나 전체를 투명하게 만드는 과정이다.

#### Who founded this?

알파 컴포지팅의 개념은 1970년대 말 앨비 레이 스미스(Alvy Ray Smith)가 처음 선보였고 1984년에 토머스 포터(Thomas Porter)와 톰 더프(Tom Duff)에 의해 논문을 통해 완전히 개발되었다

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

특징: 색 표현력이 높아 있는 그대로의 색을 재현한다. 화려한 색상과 인쇄가 필요 없는 웹, 모바일용 이미지에 적합하다.

#### CMYK(Cyan, Magenta, Yellow, Key=Black)
: 인쇄용 컬러

시안(Cyan), 마젠타(Magenta), 옐로(Yellow)의 혼합과 키(Key)컬러 블랙의 추가로 표현된다. 혼합할수록 색이 어두워진다.

- 감산혼합(subtractive color mixing): 혼합한 색이 원래의 색보다 명도가 낮아지도록 색을 혼합하는 방법

![alt text](https://upload.wikimedia.org/wikipedia/commons/2/24/SubtractiveColorMixingII.png)

확대하면, 4가지의 색상으로 이루어져 있다

![alt text](https://designmanagementlucerne.files.wordpress.com/2013/10/30.png)

특징: 색 표현력이 제한적이라 RGB보다 풍부한 색 표현이 불가능하다. 인쇄시 색감 차이가 적어 인쇄할 때 사용한다.
