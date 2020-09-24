# Week 3: What is LUT?

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
## What is the main difference with sRGB, why and when we use?

: Generate logarithmically spaced vectors

로그공간 함수는 로그 간격 벡터를 생성한다. 특히 주파수 벡터 생성에 유용하며, linspace와 ":" 또는 콜론 연산자와 동등한 로그 값이다.

y = logspace(a,b)는 10^a와 10^b 사이의 50개의 로그 간격 점의 행 벡터 y를 생성한다.

y = 로그스페이스(a,b,n)는 10^a와 10^b 사이에 n개의 포인트를 생성한다.

y = 로그스페이스(a,pi)는 10^a와 pi 사이의 포인트를 생성하며, 이 간격에 걸친 주파수가 단위 원을 도는 디지털 신호 처리에 유용하다.

### Log space reduction

A log-space reduction은 A타입의 문제를 매우 적은 메모리를 사용하는 B타입의 문제로 변환시키는 알고리즘이다. 간단한 예시로는 계산 로그/초과로 곱셈을 줄이는 것이다. 문제 A를 문제 B로 줄이고 싶은 이유는 우리가 문제 B를 해결하는 방법을 알고 있기 때문에 이를 문제 A를 해결하는데 사용하고 싶기 때문이다. A 문제가 어렵다고 믿기 때문에, 만약 우리가 A 문제를 B 문제로 축소 된다면, B 문제가 적어도 A만큼 어렵다는 것을 의미한다. 인접한 두 노드가 동일한 색상이 되지 않도록 3가지 색상으로 그래프의 노드를 효율적으로 칠할 수 있다면, 한 묶음의 무게를 같은 무게의 두 세트로 효율적으로 나눌 수도 있다.

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


