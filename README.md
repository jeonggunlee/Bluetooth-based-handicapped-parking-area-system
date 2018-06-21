## 블루투스 비콘기반 장애인 주차장 관리 시스템 - KKKK
###### 팀원 : 권용현, 김민승, 김동영, 김재현
##### 목차

1. 프로젝트 개요 및 목적
2. 프로젝트 설명
3. 프로젝트 결과
4. 프로젝트 시연영상

**프로젝트 개요 및 목적**

> 2018년 초 유명 연예인이 장애인 주차구역에 불법주차를 한 기사가 올라왔다. 이뿐만 아니라 많은 사람들이 장애인 주차구역인 것을 알면서도 불법으로 주차하는 사람들이 많이 존재한다. 그렇지만 장애인 주차구역에 일반인 차량이 세우지 못하도록 조치한 구역은 많지 않다. 사회적 약자인 장애인을 위한 주차구역을 만들고 그 주차구역을 일반인들이 어긴다면 사회적 배려를 위하여 만든 주차구역이더라도 문제가 해결되지 않는다고 생각한다. 그래서 해당 문제를 해결하기 위해서는 장애인 주차구역에 주차하기 전에 주차하려는 차량이 장애인 차량인지를 파악을 한 후 주차를 할 수 있도록 통제하는 수단이 필요하다고 생각했다. 해당 프로젝트에서는 장애인 차량인지를 파악하는 수단으로 비콘을 사용하여 통제하며 이에 대한 정보는 데이터베이스 안에 있는 장애인 차량 주소를 읽어와서 비교하여 장애인 차량인지 아닌지를 판별하도록 한다. 또한 장애인 주차장에 일반 차량이 침범하여 장애인 주차 구역 사용 인원이 불편함을 겪지 않도록 방지해주는 시스템을 영상처리를 통해 구현한다. 이러한 구현을 통하여 사회적 약자인 장애인 주차구역에 일반인들이 주차하는 불법주차를 미연에 방지하기 위함이 과제의 목적이다. 

![kakaotalk_20180621_165931757](https://user-images.githubusercontent.com/37283217/41706307-6e52236e-7576-11e8-9ad9-e97ed6a408f6.png)
![kakaotalk_20180621_165933957](https://user-images.githubusercontent.com/37283217/41706581-1d561d48-7577-11e8-90dd-ec7ca7bca0d2.png)

**프로젝트 설명**

> 장점으로는 장애인 주차구역에 일반 차량이 세울 수 없도록 미연에 방지를 해주는 것이 가장 큰 장점이며 일반 차량이 장애인 주차 구역 옆에 세울 시 주차 라> 인을 침범하여 주차하여 장애인 주차 구역을 이용하는 사람들에게 불편함을 주는 것 또한 미연에 방지할 수 있다. 구체적인 기술로는 HM-10을 통한 차량용 비> 콘 구현, 제누이노 101을 이용한 주차장 비콘 구현, 라즈베리 파이와 아두이노 간의 시리얼 통신을 통한 주차장 관리 시스템 구현, 주차장 관리 시스템 구현
> 을 위한 데이터베이스 활용, 주차장 현황을 알려주기 위한 웹사이트 구현, 라즈베리 파이에서 OpenCV를 활용하여 템플릿 매칭을 통한 차선 침범 유무 판단 시> 스템 구현 이러한 기술들을 활용하여 장애인 주차 구역 시스템을 구현하였다. 
>  <설명-1>
> 차량용 비콘의 MAC 주소들을 주차장 라즈베리 파이의 장애인 차량 주소를 가지고 있는 데이터베이스에 저장을 하여 장애인 차량이 들어왔을 때 해당 차량이 장> 애인 등록 차량인지를 판별하여 시스템을 동작시킬 수 있도록 구현한다. 또한 주차장 현황을 표현하기 위한 데이터베이스 또한 존재하며 차량이 주차되어 있는> 지에 대한 판단은 초음파센서를 통해 거리 값이 일정 이하일 경우에 차량이 있는 것으로 판별하여 데이터베이스에 update를 통하여 갱신을 해준다. 
>  <설명-2>
> OpenCV를 통하여 기존 차선에 대한 temp 이미지를 추출하여 해당 temp 이미지를 통하여 템플릿 매칭을 하여 유사도가 일정 값 이상일 경우에는 차선 침범이 > 없는 것이며 일정 값 이하일 경우에는 차선 침범이 있다는 것으로 간주하고 경보음 신호 및 경고등을 켜준다.
