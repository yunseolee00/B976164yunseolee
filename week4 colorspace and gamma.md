color space(색공간)
============


색의 3요소인 색상,명도,채도를 공간좌표에 나타낸것을 색공간(colorspace)색체계(color system)이라고 한다.
--------------------------------------------------------------------------------------------




휘도 성붙색을 표현할때 RGB를 쓰면 데이터가 너무 많고 처리가 어렵기 떄문에 사람눈에 민감한 휘도 성분(Y)과 덜 민감한 색성분(UV)을 분리한다.
------------------------------------------------------------------------------------------------------------------------




>개머트(Gamut)
모든 색공간에는 개머트라는 해당 시스템이 재연할수 있는 색상 범위가 있으며 '색영역'이라 표현하기도 한다. 사용 및 구현 가능한 색 영역에 따라 'sRGB72%, sRGB 100%, Adobe RGB99%지원'과 같은 방법으로 표기하기도 한다.



![KakaoTalk_20200927_145208941](https://user-images.githubusercontent.com/70967822/94362483-91065c00-00f6-11eb-8b9a-69784675f484.png)



RGB
====



컬러 표현을 빛의 3원색인 RED,GREEN,Blue를 서로 다른 비율로 결합하여 생성.



컬러 모니터와 같은 주로 컴퓨터 색체계에서 사용.



CMYK
====



Cyan,magenta,yellow,black을 기본으로 하여 주로 컬러 프린터나 인쇄시에 사용




YUV
===



Y축은 밝기 성분을 U,V 두축을 이용하여 색상을 표현한다. U축은 파란색에서 밝기 성분을 뺀 값이고 V축은 빨간색에서 밝기 성분을 뺀 값이다. 아날로그 컬러신호 변환에 주로 사용.



YCbCr
=====


 디지털 텔레비전 시스템에서 사용하는 색공간. 



RGB vs YUV
==========

![KakaoTalk_20200927_145209060](https://user-images.githubusercontent.com/70967822/94362863-20147380-00f9-11eb-9ff8-17f7ba3ee7fd.jpg)


•RGB는 Red, Green, Blue 빛의 3가지 속성으로 영상을 표현하는 
방식을 말합니다. 일반적으로 PC의 모니터 등에서 많이 사용됩니
다. RGB 방식에서 흑백을 표현하기 위해서는 R=G=B 3개의 채널 
값이 동일하면 흑백으로 표현됩니다. (빛의 가산 혼합)



![KakaoTalk_20200927_145209169](https://user-images.githubusercontent.com/70967822/94362893-4508e680-00f9-11eb-8d4a-03f35c655a5d.jpg)



YUV는 빛의 밝기를 나타내는 휘도(Y) 신호와 색상신호 2개(U,V)로 표현하는 방식을 말합니다. 일반적인 TV나 비디오 카메라에서 많이 사용됩니다. YUV에서는 흑백을 표현하기 위해서는 Y 신호만 있으면 됩니다.
 
•흑백 TV 시절까지 거슬러 올라가면, 흑백 TV는 빛의 밝기 신호만 가지고 영상을 표현 
했습니다. 그러다가 칼라 TV가 출현하게 되자 고민이 시작된다.
•흑백 TV와 칼라 TV를 동시에 볼 수 있게 해주는 방송 신호. 이것이 바로 YUV의 시작입 
니다. 즉, 흑백 TV는 휘도(Y) 신호만으로 영상을 보여주고, 나머지 칼라신호(U,V)는 버
립니다. 칼라 TV에서는 Y신호와 U,V 신호를 모두 이용해 칼라 화면을 보여줍니다.
 
흑백 TV가 사라진 오늘날에도 YUV 신호를 사용하는 이유는 RGB신호에 비해 압축률을
크게 향상시킬 수 있다는 점 때문입니다. RGB를 압축하여도 YUV에 비하여 상당히 많
은 데이터들이 필요로 한데, 특히 흑백만을 표현할 때도 RGB에는 모든 데이터들이 필
요하기 때문에 상대적으로 많은 저장공간을 필요로 하게 됩니다. RGB에서 YUV로의 변
환 만으로도 1/2 정도의 데이터를 줄이게 됩니다. 



-------------------------------------------------------------------------------------



Gamma, Linear workflow
=====================



Linear 은 실제색을 표현하는 반면 GAMMA는 실제색보다는 사람이 자연스럽다고 느끼는 색을 만들어낸다. Linear은 선형적인 이라는 뜻인데 그래프 처럼 왜곡되지 않은 색이다.
(sRGB는 표준감마 공간 뜻한다)



![LinearRendering-LightingSphereLinearGamma 1](https://user-images.githubusercontent.com/70967822/94363498-771c4780-00fd-11eb-8d7e-40632ebbe400.png)




![imageU09WNNS3](https://user-images.githubusercontent.com/70967822/94363677-d2026e80-00fe-11eb-9a1c-fdf5736c505c.png)




![yest359 1](https://user-images.githubusercontent.com/70967822/94363785-adf35d00-00ff-11eb-8816-31abf01ca855.png)



* Real World → Gamma 1
* sRGB Image (8 bit) → Gamma 0.45
* Float Image (32 bit) → Gamma 1
* Monitor → Gamma 2.2


[참고문헌](https://forum.reallusion.com/308094/1-PBR-Linear-Workflow)


---------------------------------------------------------------------------------



What is LUT(look up table)???
=============================



Look Up table(LUT)는 색상, 채도, 조도를 수학적으로 정확하게 조정하여 원본이미지의 RGB값을 새로운 RGB값으로 만들어주는 방법이다. 순란표 혹은 룩업 테이블은 컴퓨터 과학에서 일반적으로 배열이나 연관 배열로 이루어진 데이터 구조로, 런타임 계산을 더 단순한 배열 색인화 과정으로 대체하는데 자주 쓰인다. 처리 시간의 절약은 중요할 수 있는데, 이는 메모리로 부터 값을 받아오는 것이 입출력 기능을 거치는 것보다 더 빠르기 때문이다. 테이블들은 정적인 프로그램 저장소에 미리 계산 되어 저장되어 있거나, 프리페치 할수도 있다.
------------------



>인터넷상에는 많은 LUT 샘플들이 생겨서 손쉽게 색보정 정보를 찾아 입력할수 있다.



![luts-example 1](https://user-images.githubusercontent.com/70967822/94342839-e8e98800-004e-11eb-9f64-d12f2f92c31d.jpg)




1D LUT
======
![R800x0 1](https://user-images.githubusercontent.com/70967822/94342878-3e259980-004f-11eb-9d7c-892705fbb2e8.png)



1D LUT는 커브곡선이나 커브를 움직이는 보정값과 1:1로 매치된다. 그리고 rgb 역시 3개의 채널별로 LUT를 만든다. lift, gamma, gain, curve는 모두 R, G, B 채널별로 값을 보정할수 있고, 이 보정된 값은 1D LUT에 그대로 적용된다.


3D LUT
======
![Cube-o-Scope-1 1](https://user-images.githubusercontent.com/70967822/94342643-52689700-004d-11eb-9d01-afdc66a020c6.png)



3D LUT에서는 1D LUT에서는 표현 하지 못하는 Hue, saturation까지 담을 수 있다. 이러한게 가능한 이유는 3D LUT에서는 X,Y,Z 축의 공간좌표로 표현하기 때문이다. 위는 3D 큐브 라고도 한다.



![maxresdefault 1](https://user-images.githubusercontent.com/70967822/94344105-f9523080-0057-11eb-9982-3f26b87cd3b8.jpg)





[reference](https://blog.naver.com/canny708/221896612778)
-----------------------------------------------------------------





What is Logspace and what is main difference with sRGB, why and when we use?
========================================================================



LOG는 log함수를 이용하여 bit depth에 DR(dynamic range)와 gradation을 저장하는 방식이다.  SRGB보다 효율성있게 적은 용량으로 저장할수 있다.
------------------------------------


![Log-Curve 1](https://user-images.githubusercontent.com/70967822/94343683-bfcbf600-0054-11eb-90e4-ec6771724042.jpg)


LOG 색상 곡선을 사용하는 가장 큰 이유는 카메라 센서(또는 필름 음극)에서 가장 역동적인 정보 범위를 유지하는 방법이다. 카메라가 보는 것을 로그로 인코딩해 이미지 노출(정지 측정)과 기록된 이미지 사이의 상관관계가 더 넓은 범위에서 완전히 일정하다는 의미다. 사람의 눈이나 비디오 화면을 위해 특별히 캡처하기보다는 최대한 많은 데이터를 저장하기 때문에 표준 영상 곡선보다 센서 정보를 더 많이 활용한다. 이것은 생산 후 작업할 수 있는 훨씬 더 많은 컬러 데이터를 제공한다.




![LogWorkflow_Featured-1000x576 1](https://user-images.githubusercontent.com/70967822/94343729-205b3300-0055-11eb-840c-cdbdbda519bf.jpg)



LOG의 상단 곡선은 Linear보다 전체적으로 내려가고 하단은 올라가면서 어두운 영역도 잘보이고 너무 밝은 부분도 데이터가 보일수 있게 조정하준다. 그래서 LOG에 대한 지식은 CG에서 매우 중요한 영역이다.



[참고문헌](https://www.artstation.com/tiberius-viris/blog/3ZBO/color-space-management-srgb-linear-and-log)



[참고문헌2](https://www.rocketstock.com/blog/tips-for-log-color-space-compositing/)
