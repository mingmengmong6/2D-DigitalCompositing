# Week 2 
## What is Digital Compositing?

### Digital compositiong (디지털 합성)

연속된 이미지를 모아 디지털로 최종 이미지를 합성하는 과정. 일반적으로 인쇄, 동영상 또는 화면 디스플레이를 위해 사용된다. 디지털 컴포지팅에 사용되는 기본 연산을 '알파 블렌딩'이라고 알려져 있다.

알파 블렌딩(Alpha Blending) : 픽셀값을 주는 기능으로서, 반투명인 객체를 렌더링한다. 256단계까지 표시 가능하며 액체나, 보이지 않거나 부분적으로 보이지 않는 객체에도 적용 가능하다. 일반적으로 폭발, 물, 불과 같은 특수효과를 묘사하는데 주로 사용된다.

#### Techniques

- Blue or Green screen(블루/그린스크린)

화면을 합성하기 위해 사용되는 녹색의 스크린. 그린스크린이나 블루스크린을 배경으로 찍은 화면에서 녹색이나 푸른색을 옵티컬 프린터(optical printer)를 사용해 빼내서 합성하려는 화면과 결합하여 특수한 효과를 준다. 한국은 푸른색을 많이 사용하며 미국은 주로 녹색을 사용한다.

![alt text](https://lc2702ct1ih1dgpgj15zgyn1-wpengine.netdna-ssl.com/wp-content/uploads/2017/12/crewcallsupret-1204x630.jpg)

- Rotoscoping(로토스코핑)

실사 이미지를 종이나 셀 위에 투사하여 한 프레임씩 윤곽선을 그린 뒤 이 윤곽선을 바탕으로 애니메이션을 만든 다음 원본 이미지와 합성하는 기법. 실사 이미지와 애니메이션이 동일한 숏 내에서 동시에 연기하는 장면이 최종 결과물로 재현된다.

![alt text](https://dbscthumb-phinf.pstatic.net/4004_000_1/20151028111432679_POON5XVPM.jpg/s_ei217_11_i1.jpg?type=w492_fst_n&wm=Y)

- Particle Effects(입자 효과)

독립적인 물체들을 잘게 나누고 제작자의 의도에 맞게 조정하여 효과적으로 표현하는 방법. 많은 물체들을 하나의 파티클로 표현하고 실제 물체의 위치와 움직임을 추적하여 자연스런 영상을 만들어낸다.

![alt text](https://tutexpert.com/wp-content/uploads/2013/10/airplaine-composite-1024x576.jpg)

- Matte Painting(매트 페인팅)

실사 장면이나 애니메이션과 결합하여 영화 속 특정 공간을 묘사하거나 구성하는 고도로 사실적인 그림. 매트(matte)가 불필요한 영역을 가리면서 필요한 그림이 노출될 수 있도록 유리판 위에 그림을 그려 촬영하는 기법. 이야기 속 공간 배경이 실제로 존재하지 않거나 실제 공간을 촬영할 수 없을 경우, 또는 원하는 피사체를 미니어처나 모델로 제작하는 것이 비효율적일 경우 현실감의 극대화를 목표로 하여 정교하게 수행한다.

![alt text](https://cdnb.artstation.com/p/assets/images/images/006/143/817/large/paul-mercer-ancient-civilisations-artstation-challenge-temple-ruins-01-copy.jpg?1496337756)

- Motion Capture(모션 캡쳐)

몸과 얼굴의 자연스러운 움직임을 기록하여 디지털 캐릭터를 제작하는 기법. 실제 동물이나 사람의 연기를 원판으로 삼아 CGI로 만들어지는 캐릭터의 자연스러운 연기를 재현하는 시각효과. 표정 연기의 추출을 위해 눈꺼풀을 포함한 주요 얼굴 근육에도 마커가 부착되며 표정만을 잡는 특수 카메라가 머리에 씌워진다. 수십에서 수백 대의 전자 카메라들이 자외선을 방사하고, 자외선에 반응하는 마커들의 동작을 통해 휴먼 캐릭터(human character)의 연기가 녹화된다.

![alt text](https://lh3.googleusercontent.com/proxy/0uF4zXJ7PaWohcidc07ybNCj5HRLq3KnfWP3HEHYX9hb6Mj7OZ-S0qJ4itRsuCts1ocLjLVLXtVAUozM4Yxlvdj8u0DvdcwOYmfKVb8-PVW-HHPHMCsY1yUlxTGQeO5Neg)

- Digital Actor(디지털 배우)

3차원 CG(Computer Graphics) 기술로 만든 가상의 배우. 실제 배우 수준의 외형과 동작을 가진 배우로, 얼굴 표정, 피부, 머리카락 표현 등의 섬세함은 물론 동작이 자연스러워야 하는 고도의 기술이 요구된다.

![alt text](https://www.fxguide.com/wp-content/uploads/2013/11/compare-actor.jpg)

- Morphing(모핑)

하나의 이미지를 다른 이미지로 연속적으로 변형시키는 디지털 시각효과, 일정한 시간 내 여러 형상을 거쳐 최종 이미지로 변화되는 모습을 재현한다. 하나의 이미지를 다른 것으로 변형시키는 데 필요한 변화를 컴퓨터가 수학적으로 계산하는 과정을 거친다. 먼저 변형되는 이미지와 변형될 이미지 사이의 유사점을 찾아 서로를 매치(match)하는 과정이 필요하다. 변형에 필요한 시간값을 입력하면 컴퓨터 소프트웨어가 매칭이 된 부분의 색상과 형태의 변화에 필요한 부분을 계산하여 입력한 시간 동안 자연스럽게 변화시키게 된다.

![alt text](https://ccrma.stanford.edu/~jacobliu/368Report/ah_morph.jpg)

#### Layer-based vs. Node-based compositing

2가지의 Work flow(워크플로우)가 존재: Layer-based compositing와 Node-based compositing

|  Layer-based        | Node-based       |
| ------------------- | -----------      | 
|  comlicated         | more complicated |
|  3d place           | Real 3d space    |

#### Layer-based compositing


|stacking order|
| ------------ |
|layer1        |
|layer2        |
|layer3        |
|layer4        |
|layer5        |

-> 오래된 작업순으로 레이어를 쌓아간다. 타임라인과 이펙트, 키프레임을 포함한 개별적인 레이어로 구성되어 있다.
 빠른 2D 및 모션 그래픽과 같은 제한된 3D 효과에 적합하지만, 많고 복잡한 레이어를 갖는 컴포지트에는 어색해진다.
 
ex) After Effects

#### Node-based 


미디어 개체를 맵에서 연결한다. 이전 이미지 처리단계인 "context"의 파라미터를 수정할 수 있는 기능을 포함한 매우 유동적인 방법이다. Work flow(워크플로우)는 레이어 기반 컴포지팅과 달리 타임라인에서 직접적으로 연결되지 않기 때문에 종종 키프레밍과 시간 효과를 제대로 처리하지 못하는 문제가 발생한다.

![alt text](https://i.stack.imgur.com/Biirj.png)

ex) Nuke, Fusion, Blender


## What is Alpha and Digital color?

### Alpha

#### Alpha compositing

알파 컴포지팅은 하나의 이미지를 배경과 결합하여 부분적으로나 전체를 투명하게 만드는 과정이다.

#### Why and Who founded this?

알파 컴포지팅의 개념은 매트정보를 저장하기 위해 1970년대 말 앨비 레이 스미스(Alvy Ray Smith)가 처음 선보였고 1984년에 토머스 포터(Thomas Porter)와 톰 더프(Tom Duff)에 의해 논문을 통해 완전히 개발되었다

#### Description

각 픽셀의 색상을 저장하는 2D 화소(픽셀)에서는 0~1의 값을 갖는 알파 채널에 추가 데이터가 저장된다. 

0의 값 -> 픽셀이 투명하고 수치 정보를 제공하지 않음, 1의 값 -> 지오메트리가 픽셀 윈도우와 완전히 겹치기 때문에 픽셀이 완전히 가림.

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Alpha_compositing.svg/1284px-Alpha_compositing.svg.png)
### Color

#### 색의 3원색 ≠ 빛의 3원색

색의 3원색: 빨강, 파랑, 노랑 // 빛의 3원색: 빨강, 초록, 파랑, 

#### 색의 3속성
- 색상(Hue): 색을 구별하는 속성

색상환에서 거리가 가까운 색은 유사색, 거리가 비교적 먼 색은 색상차가 커서 대조색, 거리가 가장 먼 정반대쪽의 색은 보색.

![alt text](https://search.pstatic.net/common/?src=http%3A%2F%2Fcafefiles.naver.net%2F20130327_83%2Fi_pang_1364372973772JTEfk_JPEG%2F%25B8%25D5%25BC%25BF%25C0%25C720%25BB%25F6%25BB%25F3%25C8%25AF.jpg&type=sc960_832)

- 명도(Saturation): 색의 밝고 어두운 정도, 색의 밝기

 0-3단계는 저명도, 4-6단계는 중명도, 7-10단계는 고명도

- 채도(Value): 색의 강약과 선명한 정도

높은 채도의 순색, 순색에 흰색이나 검은색을 혼합하여 본래의 색보다 밝아지거나 어두워진 색의 청색, 순색에 회색을 혼합하여 탁하거나 낮은 채도의 탁색(흐린 색)

![alt text](https://lightcolourvision.org/wp-content/uploads/10100-0-A-BL-EN-HSB-Colour-Model-Hue-Saturation-and-Brightness-80.jpg)

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
