What is LUT(look up table)???
=============================



Look Up table(LUT)는 색상, 채도, 조도를 수학적으로 정확하게 조정하여 원본이미지의 RGB값을 새로운 RGB값으로 만들어주는 방법이다. 순란표 혹은 룩업 테이블은 컴퓨터 과학에서 일반적으로 배열이나 연관 배열로 이루어진 데이터 구조로, 런타임 계산을 더 단순한 배열 색인화 과정으로 대체하는데 자주 쓰인다. 처리 시간의 절약은 중요할 수 있는데, 이는 메모리로 부터 값을 받아오는 것이 입출력 기능을 거치는 것보다 더 빠르기 때문이다. 테이블들은 정적인 프로그램 저장소에 미리 계산 되어 저장되어 있거나, 프리페치 할수도 있다.
------------------



![luts-example 1](https://user-images.githubusercontent.com/70967822/94342839-e8e98800-004e-11eb-9f64-d12f2f92c31d.jpg)




1D LUT
======
![R800x0 1](https://user-images.githubusercontent.com/70967822/94342878-3e259980-004f-11eb-9d7c-892705fbb2e8.png)



1D LUT는 커브곡선이나 커브를 움직이는 보정값과 1:1로 매치된다. 그리고 rgb 역시 3개의 채널별로 LUT를 만든다. lift, gamma, gain, curve는 모두 R, G, B 채널별로 값을 보정할수 있고, 이 보정된 값은 1D LUT에 그대로 적용된다.


3D LUT
======
![Cube-o-Scope-1 1](https://user-images.githubusercontent.com/70967822/94342643-52689700-004d-11eb-9d01-afdc66a020c6.png)



3D LUT에서는 1D LUT에서는 표현 하지 못하는 Hue, saturation까지 담을 수 있다. 이러한게 가능한 이유는 3D LUT에서는 X,Y,Z 축의 공간좌표로 표현하기 때문이다. 위는 3D 큐브 라고도 한다.



-----------------------------------------------------------------



What is Logspace and what is main difference with sRGB, why and when we use?
========================================================================



[참고문헌](https://www.artstation.com/tiberius-viris/blog/3ZBO/color-space-management-srgb-linear-and-log)
[참고문헌2](https://www.rocketstock.com/blog/tips-for-log-color-space-compositing/)
