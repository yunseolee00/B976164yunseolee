Digital 2D compositing week3 assignment
=======================================






<hr/>



1.About digital color
=====================



![e2c570b63f5e392ecff752c4a88c1fe659d72ace 1](https://user-images.githubusercontent.com/70967822/93712278-d45d4980-fb8f-11ea-97aa-988dc7e4cff1.png)

RGB
----

R=red  G=green  B=blue



R+G+B= white


CMYK
-----
C=cyan M=magenta Y=yellow K=black



>RGB는 빛의 삼원색으로 모니터, 조명에 관해 쓰인다.  CMYK는 주로 프린터, 인쇄에 쓰이는 색으로 색이 섞이면 섞일수록 RGB와는 반대로 어두워진다.




>     > 이 두 색이론은 서로 대조가 되기 때문에 그래서 RGB는 가법혼색(additive mixing), CMYK는 감법혼색(subtract mixing)이라고 부른다.


![commonNGUEHMZN](https://user-images.githubusercontent.com/70967822/93712471-120ea200-fb91-11ea-8c74-ebe68cef982e.jpg)






<hr/>








H/S/V
======





![HSV-color-space-Hue-saturation-value 1](https://user-images.githubusercontent.com/70967822/93712883-85191800-fb93-11ea-95da-f4a89e80ff1f.png)



H=hue(색조)
----------



색상을 정한다.



S=saturation(채도)
-----------------



색의 세기,RGB에 가까운 색을 정한다.




V=Value(명도)
-------------



white, black에 가까운 정도를 정한다.



<hr/>





2.WHat is BIT?(색심도)
===============




![05 1](https://user-images.githubusercontent.com/70967822/93713450-ef7f8780-fb96-11ea-996d-3d0b7c5bd3a6.jpg)




디지털에서는 각 색의 밝기를 숫자로 나타내어 표기하는데, 보통 각 색에 몇 비트씩 할당하여 표현한다. 비트 수에 따라 표현할 수 있는 색상 수가 달라진다.
>쉽게말해서 bit는 색의 다양성 범위이다.




![common8WC9U63H](https://user-images.githubusercontent.com/70967822/93714416-6ae43780-fb9d-11ea-8fc5-993def02b82e.jpg)

•1비트: 2개 색상만 표현 가능하다. 그 중 하나는 거의 항상 검정만 표시하기 때문에, 남은 한 색상만 달라진다. 검정과 흰색만 표현하면 흑백. 초창기에 나온 그린 모니터나 호박색 모니터가 이런 경우다.


•2비트: 네 가지 색상이 표현 가능하다. 이제는 고대유물급이게 고대 유물이면 위에는?인 단색 모니터에서는 이걸로 4단계의 명암을 표현했다. 실제로 닌텐도의 흑백 게임보이도 이 방식으로 명암을 구현한 바 있다. 컬러모니터로 넘어오고 나서는 왠지 Cyan, Magenta, White, Black의 4색으로 치환되는 경우가 많다.


•4비트: 과거 EGA 그래픽 카드가 사용했던 것으로, 16색 표현이 가능했다. 일본의 PC-9801 기종으로 나온 게임은 16색을 가지고도 도트 노가다를 통해 풀컬러나 별 차이 없어보이는 상당히 미려한 그래픽을 구현했다.


•8비트: 256색 표현이 가능. 1990년대까지 많이 쓰였다. R과 G는 3비트, B에는 2비트[3]를 할당하여 256색을 구현하는 방식으로 VGA 그래픽카드에서는 320x240 해상도에서 8비트 256칼라 그래픽 모드를 기본적으로 지원했다. 이와는 별도로 따로 색상 팔레트(Palette) 256개를 준비해 두고 실제 그래픽 메모리의 8비트는 팔레트의 인덱스를 가리키는 인덱스드 컬러(Indexed color. 또는 Pseudocolor, Indirect color) 방식도 사용할 수 있었다. 
>  Photoshop에서는 0~255으로 0에서 시작하기 떄문에 수치가 255로 되어있다.

•16비트: R과 B는 5비트, G는 6비트[4]를 할당하여 만든 색공간으로, 하이 컬러(High Color)라고 많이 불렸다. 각 색상 비트 수를 따서 565 컬러 모드라는 표현도 있었다. 65,536가지 색상이 표현 가능하다. 바리에이션으로 RGB 모두 5비트를 표현하고, 나머지 1비트는 투명 여부를 표현하는 값으로 쓰인 것도 있다. 


•24비트: RGB를 각각 8비트씩 할당한 것. 이것을 24비트 트루 컬러(True Color)라고 말한다. 이렇게 표현 가능한 색상은 16,777,216가지이고, 이것은 sRGB 에서 기본적으로 다루는 색심도로 국제전기표준회의의 표준으로 등재되어 있다. HTML의 색상 코드도 이것을 16진수로 표현한 값을 쓰고 있다.


•32비트: 24비트 트루 컬러에 8비트의 투명값(alpha)를 추가한 것으로, RGBA라고 부른다.




[참고문헌](https://namu.wiki/w/RGB)




BIT references
----------------




![Batman_8Bit_1stEdition_FINAL_v2_55fb5536247e19 25064732 1](https://user-images.githubusercontent.com/70967822/93713702-8731a580-fb98-11ea-89c8-3af7ee3a4069.gif)



**8bit**



![common8L2SP5NV](https://user-images.githubusercontent.com/70967822/93713814-5a31c280-fb99-11ea-8447-0bc3bb2efc8a.jpg)



**16BIT**



<hr/>



3.RAW and JPG
==============



![commonALZL5OFL](https://user-images.githubusercontent.com/70967822/93714063-10e27280-fb9b-11ea-92fe-b5209ee78641.jpg)



RAW: 압축 이전의 원본, 용량이 크다



JPG: 데이터를 손실압축하면서 화상으로 바꾼 이미지




<hr/>




4.RGB(0,0,0)
============



>vector (x,y,z) (r,g,b)



>float (소수점) (0.345) (1.5)



>integer (정수) (0,1,2,3...)



<hr/>



5.ALPHA channel
===============




![image](https://user-images.githubusercontent.com/70967822/93714808-01195d00-fba0-11ea-80b6-90160e572cd9.png)




