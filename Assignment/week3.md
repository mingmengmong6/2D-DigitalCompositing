# Week 3: What is LUT?
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

#### 3D LUTS
: 구체의 모양으로 색을 개별적으로 조정할 수 있다. 색상, 채도, 명도의 개별적인 축으로 보다 더 정확하게 특정 색상값을 조정하다. z, y, x축의 형태이다. 하지만 불변성을 가지고 있지 않다.


![alt text](https://s.studiobinder.com/wp-content/uploads/2019/02/What-is-LUT-LUT-Color-Grading-Ridley-Scott-Film-LUTs-Pack.jpg)


https://groundcontrolcolor.com 에서 LUT를 무료로 다운가능

출처
https://www.studiobinder.com/blog/what-is-lut/
