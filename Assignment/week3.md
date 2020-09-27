# Week 3
# 1. Color space and Gamma
## What is Color space?
색 공간(color space)는 색 표시계(color system)를 3차원으로 표시한 공간개념이다. 색의 3속성인 색상, 명도, 채도를 3차원 공간에서 각각의 축으로 형성하도록 하고 있다.

- RGB 색 공간
웹 색상 표현의 기본 원리. 색을 혼합하면 명도가 올라가는 가산 혼합 방식으로 색을 표현한다.(RG 가산 혼합의 3원색: 빨강, 녹색, 파랑) RGB 색 공간은 삼원색의 해당하는 세 가지 채널의 밝기를 기준으로 색을 지정한다.
![alt text](https://www.researchgate.net/profile/Sanjay_Antony-Babu/publication/40768762/figure/fig1/AS:601637223690242@1520452900835/Colour-space-cube-representation-of-colour-space-with-red-green-and-blue-colour.png)

- CMYK 색 공간
인쇄과정에서 쓰이는 감산혼합 방식. 흰 바탕에 네가지 잉크의 조합으로 색을 나타내는 것을 말한다. 색을 혼합하면 명도가 낮아지기에 감산 혼합이라고 한다. 4가지 색: 옥색(cyan), 자청색(magenta), 노랑(yellow), 검정(black)
![alt text](https://i.pinimg.com/originals/fc/40/1e/fc401eb9ddb361415c66445074cf8fc1.jpg)

- HSV 색 공간
색상(), 채도(), 명도()를 기준으로 색을 구성하는 방식. 감산 혼합이나 가산 혼합보다 색상의 지정이 직관적이기 때문에 시각예술에서 자주 쓰인다.
![alt text](https://i1.wp.com/www.loopandbreak.com/wp-content/uploads/2013/08/untitled9.jpg?resize=350%2C350)

# 2. What is LUT?

![alt text](https://s.studiobinder.com/wp-content/uploads/2019/02/What-is-LUT-LUT-Color-Grading-Ridley-Scott-Film-LUTs-Pack.jpg)

## LUT(Look-up table)
  Look-Up Table(LUT)는 색상(hue), 채도(saturation), 명도(brightness)를수학적으로 정확하게 조정하여 촬영된 원본 이미지의 RGB값을 새로운 RGB값으로 만들어주는 방법이다.
특정 계산의 바로 가기를 제공하는 미리 결정된 숫자의 배열을 설명하는 데 사용되는 용어로 컬러 그레이딩(Color Grading)에서 LUT는 색상 입력 값(카메라)을 원하는 출력 값(최종 영상)으로 변환한다.일반적으로 배열이나 연관 배열로 된 데이터 구조로, 런타임 계산을 더 단순한 배열 색인화 과정으로 대체하는 데 자주 쓰인다 자료를 다른 형태로 변환시키기 위한 컴퓨터 프로그램이 빠른 시간 내에 접근이 가능하도록 만들어졌다.

### Why use LUTs on footage? / 왜 영상에 LUT를 사용하는가?
- 구체적인 비주얼을 위해 미리 설정된 값을 정한다.
- 색 보정 속도를 증가시킨다.
- 참조점으로 독특한 스타일을 발전시키는데 사용할 수 있다.

#### 간단하게 말하자면, LUT는 영상의 프리셋 색상 값
LUT는 영상에 직접적으로 적용되어, 보정단계를 훨씬 더 빠르게 한다. 특정 LUT는 우리가 좋아하는 영화나 방송처럼 보이게 변형할 수 있다.

### What are LUTs for? / LUT는 어디에 사용되는가?
- 화면을 보정한다
- 나중에 사용하기 위해 색보정을 만들고 저장한다
- flat이나 log footage를 만든다
- 샷이나 보정에서 스타일을 추가한다

### What uses LUTs? / 무엇이 LUT를 사용하는가?
색을 조정할 수 있는 모든 프로그램에서 쓰인다 ex) Photoshop, Final cut, Premiere pro, etc

### LUT의 종류
: calibration, transform, viewing, 1D and 3D.

#### 1D LUTS Vs. 3D LUTS
어떠한 방식으로 이미지를 조정하느냐의 차이이다. 두 유형 모두 lookup table의 정확도를 결정하기 위해 비트 크기와 비트 깊이를 모두 사용한다.숫자가 클 수록 더 나은 색보정을 얻을 수 있다.

#### 1D LUTS
: 한 가지 설정 값으로 조정되는 단순한 색보정 방법이다. 직선의 형태이다. 하지만 3d의 이미지의 색상을 정확히 표현해 낼 수는 없다. 하지만 불변성을 갖고 있다.
- 출력 값에 대한 모든 입력 값을 가져야 한다. 입력 값은 해당 한계 내에서 정확하며 보간이 필요하지 않다.
- 밝기/대비/감마 변화에 유용하다.
- 세 가지 기본(RGB) 사이에 필요한 상호 작용이 없는 경우 색상 수정에 사용할 수 있다.
- 기본 색상 등급 지정 및 표준 색상 공간 간 변환(예: Rec.709에서 sRGB로, Rec.2020에서 Rec.709로)에 주로 유용하다.

![alt text](https://cdn.serif.com/spotlight/content/qty/8x9/hl4/1d-lut-graph--article-lg@2x.jpg)

#### 3D LUTS
: 구체의 모양으로 색을 개별적으로 조정할 수 있다. 색상, 채도, 명도의 개별적인 축으로 보다 더 정확하게 특정 색상값을 조정하다. z, y, x축의 형태이다. 하지만 불변성을 가지고 있지 않다.
- 색상 값이 서로 상대적으로 변경될 수 있기 때문에 게이머트 변경, 포화 및 채널 혼합과 같은 복잡한 작업을 처리 가능. 색깔 또한 완전히 바뀔 수 있다(파란색 -> 초록색, 반대로 초록색이 될 수도 있다).
- 3D 공간의 모든 포인트에 대해 입력 및 출력 값을 생성하면 파일 크기가 비싸기 때문에 interplation이 필요하다. interpolation 여부는 소프트웨어에 달려 있다.
- 색상 값이 예측 불가능하고 다양한 카메라 색상 공간과 사이를 변환하는 데 이상적
![alt text](https://cdn.serif.com/spotlight/content/cqf/xns/yfx/3d-cube-right--article-sm@2x.jpg)

![alt text](https://cdn.serif.com/spotlight/content/xlp/n5x/swz/3d-point-cloud--article-sm@2x.jpg)

![alt text](https://noamkroll.com/wp-content/uploads/2020/06/How-To-Apply-Color-Grading-LUTs-Professionally-My-Workflow-Explained.jpg)

https://groundcontrolcolor.com 에서 LUT를 무료로 다운가능

출처
https://www.studiobinder.com/blog/what-is-lut/

https://affinityspotlight.com/article/1d-vs-3d-luts/


# 3. What is Logspace?

Logspace: Generate logarithmically spaced vectors

로그공간 함수는 로그 간격 벡터를 생성한다. 특히 주파수 벡터 생성에 유용하며, linspace와 ":" 또는 콜론 연산자와 동등한 로그 값이다.

y = logspace(a,b)는 10^a와 10^b 사이의 50개의 로그 간격 점의 행 벡터 y를 생성한다.

y = 로그스페이스(a,b,n)는 10^a와 10^b 사이에 n개의 포인트를 생성한다.

y = 로그스페이스(a,pi)는 10^a와 pi 사이의 포인트를 생성하며, 이 간격에 걸친 주파수가 단위 원을 도는 디지털 신호 처리에 유용하다.

### Log and Color Space in Compositing
#### Log footage는 포스트 프로덕션 워크플로우에서 중요한 부분이다.
디지털 영화 제작이 점점 더 저렴해짐에 따라, 기술은 컬러리스트나 제작 후 전문가들에게 점점 더 많이 보급되고 있다. 이 경우, Log color space는 꽤 오래전부터 존재해왔다. 처음에 high end post houses들은 그것을 cineon log(시네온 로그)라고 불리는 color space에서 스캔한 film negatives와 함께 사용했다. 현재 거의 모든 카메라 제조업체는 자체 로그 곡선(또는 다중 로그)을 제공한다. S-Log 2&3(소니), LogC(아리), 캐논 로그, V-Log(파나소닉), 레드 로그필름, 블랙매직 로그 등이 있다. 이들 각각은 서로 다르며, 대개 특정 제조업체 제품의 색 과학에 맞게 조정된다.

로그 색상 곡선을 사용하는 가장 큰 이유는 카메라 센서(or film negatives)에서 가장 역동적인 정보 범위를 유지하는 방법이다. 카메라가 보는 것을 로그로 인코딩해 이미지 노출과 기록된 이미지 사이의 상관관계가 더 넓은 범위에서 완전히 일정하다는 의미다. 사람의 눈이나 비디오 화면을 위해 특별히 캡처하기보다는 최대한 많은 데이터를 저장하기 때문에 표준 영상 곡선보다 센서 정보를 더 많이 활용한다. 이것은 생산 후 작업할 수 있는 훨씬 더 많은 컬러 데이터를 제공한다.

![alt text](https://assets.rocketstock.com/uploads/2017/05/Log-Curve.jpg)

### Log vs. Linear Color Space
#### Log curve
로그 곡선은 그림자를 유지하기 위해 이미지의 어두운 부분을 위로 밀어 올린다. 곡선의 상단은 하이라이트를 유지하기 위해 아래로 이동한다. 따라서 색상 곡선의 각 측면에서 더 많은 데이터를 보존할 수 있다.

#### Linear Color Space
직선 컬러 스페이스는 씬에서 정확한 수학적 값에 참하여 일정하고 변하지 않는 휘도 값을 가진다.

우리의 눈은 정확한 휘도 값과 색을 다르게 보고 밝고 어두운 영역에서 더 자세한 것을 볼 수 있기 때문에, 이것은 어떤 부분에서는 매우 어둡고 질퍽하게 보일 것이고 다른 부분에서는 지나치게 노출될 것이다. 따라서 우리는 색 정보를 좀 더 미적으로 보기 위해 다른 색 공간을 적용해야 하고, 디스플레이와 모니터의 색 값을 표준화해야 한다.

## What is the main difference with sRGB, why and when we use?
### Linear vs. sRGB
직선 color space에서, 저장된 숫자와 그것들이 나타내는 값 사이의 관계는 직선 1:1 비율이다. 예를 들어 숫자를 두 배로 늘리면 강도가 두 배가 된다는 것을 의미한다. 그것은 쉬워보이지만, 문제는 빛에 대한 인간의 눈 감도가 높은 강도보다 낮은 강도에서는 훨씬 더 미세하다는 것이다. 특히 값을 나타내기 위해 8비트를 사용한다면(총 256개의 음영), 너무 많은 밝은 음영을 사용하게 되고, 충분히 어두운 그림자를 갖지 못한다. [그림 1].
그러므로 linear 공간은 컴퓨터 프로세싱에 사용하기에 완벽하지만 우리의 눈은 같은 간격의 밝기 변화를 거의 같은 간격으로 볼 것으로 예상하기 때문에 인간의 시야에 적합하지 않다. 예를 들어, 우리의 뇌는 그늘이 16보다 두 배, 그늘이 48 (32+16과 같은)이 32보다 두 배 밝기를 기대한다. 이 문제를 해결하기 위해 대부분의 최신 모니터는 sRGB의 변환을 적용하는데, 감마선을 사용하여 색상을 비직선적으로 만드는 표준이다[그림 2]. 곡선은 아래쪽보다 얕아서 어두운 값을 더 많이 표시할 수 있고, 위쪽에 더 가파르게 표시할 수 있어 더 적은 빛의 값을 가질 수 있다.

[그림 1]
![alt text](https://cdnb.artstation.com/p/media_assets/images/images/000/394/819/medium/image00.jpg?1552184196)

[그림 2]
![alt text](https://cdna.artstation.com/p/media_assets/images/images/000/394/820/large/image02.jpg?1552184260)

우리는 우리의 이미지가 컴퓨터 친화적이지만 인간 친화적인 sRGB에 저장되는 직선적 공간에서 처리되기를 원한다. 하지만, 이미 8bit 직선에는 충분히 어두운 그림자가 없다는 것은, 직선으로 바꿀 때 문제가 될 수 있다. 이와 같이, 우리가 발견한 해결책은 8bit에서 16/32bit로 범위를 넓혀서 작업하기에 훨씬 더 어두운 색조를 갖는 것이다. 이러한 종류의 이미지는 HDR(high dynamic range)이라고 불리며 일반적으로 32bit OpenEXR(.exr)로 저장된다.


대부분의 Photoshop 툴은 8bit 또는 16bit 모드에서만 제대로 작동하며, 32비트 선형 이미지를 일반 8/16bit sRGB 작업 공간에서 다시 보려고 할 때 발생하는 두 가지 문제가 있다.

1. 소프트웨어가 모든 정보를 표시하는 방법을 알 수 없다면 관리되지 않는 32비트 직선 이미지는 매우 높은 대비를 나타낼 것이며, 이는 매우 어두운 중간 톤과 지나치게 노출된 하이라이트를 의미한다[그림 3]. 이 문제의 일부는 역 감마선을 적용하여 해결할 수 있다.
2. 32bit HDR 이미지를 8bit LDR equivalent로 변환하는 것은 파괴적인 과정이다. 애초에 저장하려고 했던 추가 정보가 모두 손실되고 있기 때문이다. 이를 보통 'value clipping(값 클리핑)'이라고 부르기 때문에 합성자가 그림의 범위가 충분치 않거나 '클립'되었다고 말할 때, 일반적으로 하이라이트나 그림자에 충분한 디테일이 없다는 것을 의미한다. 참고: 8bit 작업 공간에서 그림을 시작하고 만든 다음 컴프로 전달할 때도 이러한 현상이 발생함

[그림 3]
![alt text](https://cdnb.artstation.com/p/media_assets/images/images/000/185/191/medium/comparison2.jpg?1516129275)

 포토샵 툴은 8비트 또는 16비트 모드에서만 제대로 작동하기 때문에 32비트 형식으로 이용 가능하거나 대부분의 정보를 유지하는 그런 모드에서 그림을 그릴 수 있는 방법을 찾아야 한다. 
 #### So, this is why Log exists 그래서 로그가 존재한다!
 
 #### Log (short for logarithmic)
로그는 color space "archiver"로 생각할 수 있다(zip 또는 rar의 파일과 같은 방식). 이는 직선 공간은 동일한 단계로 값을 증가시키지만 Log color space은 이미지의 흰색과 검은색 영역에 있는 값을 압축하여 정보를 저장하는 데 필요한 공간을 최소화하기 때문이다[그림 4].

[그림 4]
![alt text](https://cdnb.artstation.com/p/media_assets/images/images/000/394/821/medium/image01.jpg?1552184324)

### Log Painting Workflow for Matte Painting / 매트 페인팅을 위한 로그 페인팅 워크플로우
로그 플레이트를 직선의 값으로 변경했든 간에 정확한 페인팅을 위해 우리는 색 조정을 해야한다.

1. Displaying the log material with the target LUT

"log" 이미지는 큰 다이나믹 range를 나타내기 때문에 대부분의 중간톤 픽셀은 coding space의 중간 부분에 위치한다. 따라서 일반 sRGB 모니터에 'log' 영상을 직접 표시하면 대비가 약하고 불포화도가 낮은 색상으로 나타나므로 올바른 색의 플레이트를 미리 보기 위해서는 색 조정이 필요하다. 포토샵에서 이것을 하는 방법은 Log 이미지의 색과 값을 타겟 프로파일처럼 보이게 하기 위해 소프트웨어에 톤 맵을 하는 LUT를 기반으로 한 'Color Proof' 미리보기를 적용하는 것이다. 이 디스플레이 변환은 이미지에 구운 것이 아니며 color space를 보존하려는 것이므로 미리 보기만 유효하다.
Tip: under View>Proof Setup, CTRL+Y를 누르면 색상 값를 빠르게 설정하거나 해제할 수 있다. 특히 어둠 값에서.

2. Converting reference images to the log color space

매트 페인터들은 보통  photo refs를 갖고 공간을 만든다. 문제는 같은 카메라에서 만들어지지 않는 한 일반적으로 8비트 sRGB로 다른 포맷으로 만들어질 가능성이 매우 높다. 플레이트를 보존하고 우리에게 제공된 것과 같은 공간에서 페인팅을 전달할 생각이므로 레퍼런스를 사용하기 전에 변환해야 한다. 이것의 3가지 방법이 있다.(점점 더 좋은 순)
- 조정 레이어: 눈이 매우 예리한 경우 로그 공간에 대한 레퍼런스를 일치시키기 위해 Curves, Hue/Saturation and/or Color Balance과 같은 조정 레이어와 매치 해야한다. 그렇게 하는 동안, 당신은 모든 레벨이 일치하는지 확인하면서 color proofing을 끄고 플레이트의 raw, 낮은 대비를 보아 모든 값을 일치시켜야 한다.

- Photoshop 변환: 컬러 조회 조정 레이어를 사용하고 3D LUT 파일을 불러와 포토샵에서 직접 레퍼런스를 변환할 수 있다. 그러나 이 방법은 정확한 LUT 파일을 제공하는 데 의존하며 오류가 발생하기 쉬우므로 변환 후 모든 항목을 확인해야 한다.

- Nuke 변환: 만약 Nuke에 접근할 수 있다면, 그 안에 ref를 가지고 와서 적절한 color space에 그것들을 쉽게 출력할 수 있다. 이 과정은 심지어 스크립트의 도움으로 자동화될 수 있고, 또한 가장 정확하다

3. Converting back to linear

앞서 살펴본 바와 같이, compositing, lighting, lookdev와 같은 다른 모든 CG workflow/pipelines들은 직선 공간 처리를 기반으로 한다. 우리는 로그 공간만을 이용해서 우리가 쉽게 사용하고 있지만, 페인팅을 완성하고 나면 32비트 직선으로 다시 변환해서 다른 단계에서 사용할 수 있도록 해야 한다.
가장 쉬운 방법은 Nuke에서 변환을 하는 것이지만, 스튜디오마다 자체 변환 툴이 있으니 먼저 확인하자.


출처 
https://www.rocketstock.com/blog/tips-for-log-color-space-compositing/

https://www.artstation.com/tiberius-viris/blog/3ZBO/color-space-management-srgb-linear-and-log
