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

>INDEX이미지: 모든 이미지를 256컬러(8bit) 이하로 낮춰준다


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



>float () (0.345) (1.5)



>integer (정수) (0,1,2,3...)



<hr/>



5.ALPHA channel
===============




![image](https://user-images.githubusercontent.com/70967822/93714808-01195d00-fba0-11ea-80b6-90160e572cd9.png)



>알파 채널(영어: alpha channel) 또는 알파 합성(영어: alpha compositing)은 α 채널과 이미지 처리 분야에 있고, 각 화소에 대해 색상 표현의 데이터로부터 분리한 보조 데이터를 일컫는다. [출처}(https://ko.wikipedia.org/wiki/알파_채널)



1.Non-premultiplied alpha(straight alpha)
------------------------------------------

![9975123B5C0FD14335 1](https://user-images.githubusercontent.com/70967822/93715174-a2091780-fba2-11ea-81da-9a3e807ac437.png)



"non-premultiplied alpha"는 "straight alpha" 또는 "unassociated alpha"라고도 부르며, 우리가 가장 익히, 편하게, 친숙하게 알고 쓰는 알파 형식입니다.

이를 테면, HTML/CSS에서 색상을 표현할 때 쓰는 RGBA 포맷이 straight alpha를 적용하고 있습니다.

straight alpha 방식의 RGBA는, 알파 값만이 화소의 투명한 정도를 나타내며, RGB 각각의 값은 투명도와 관계 없이 빨강, 초록, 파랑의 강도를 표현합니다.

가령, 아래처럼 RGBA 형식으로 표현되는 화소가 있다고 할 때,

rgba(255, 200, 0, 0.4) // RGB는 0~255 사이 정수

상기한 RGBA는 대략 이런 뜻입니다.

R: 100% 강도의 붉은 빛을 내며, (255는 최대)
G: 78% 강도의 초록 빛을 내며, (200은 중간 78% 지점)
B: 0% 강도의 푸른 빛을 내며, (0은 최소)
A: RGB 세 가지 각각의 빛의 세기를 그 40% 만큼으로 줄여서, 불투명도를 40%로 떨어뜨린다. (60% 투명해 보이게 한다.)



2.Premultiplied alpha
---------------------



![99C8A5495C0FD14314 1](https://user-images.githubusercontent.com/70967822/93715147-75550000-fba2-11ea-950b-e2e79b3a27de.png)



premultiplied alpha 방식의 RGBA 인코딩은, 그 이름이 암시하듯이 알파 값을 RGB에 미리 곱해 둡니다.

RGB에 (불)투명도를 미리 곱해 두면, 알파 값 없이 RGB만 가지고도 투명도가 적용된 색상을 얻을 수 있을 뿐만 아니라, 그래픽 처리시에 필요한 연산이 줄어드는 장점이 있죠.

다시 말해 premultiplied alpha 방식의 RGBA에서 RGB의 값은 그 자체만으로도 색상과 더불어 이미 투명도를 반영하고 있으며, 알파 값은 복잡한 그래픽 처리를 위해서 덤으로 딸려 들어오는 것에 불과합니다.

그리고 이 방식의 또 한 가지 특징은 RGB 각각의 값이 덤으로 얹어 주는 알파의 값보다 항상 작거나 같다는 점입니다.

예를 들어, 위에서 사용했던 예시와 같은 straight (non-premultiplied) RGBA가 있다고 합시다.

rgba(255, 200, 0, 0.4) // RGB는 0~255 사이 정수

이를 premultiplied RGBA로 표현하면 다음과 같습니다.

rgba(102, 80, 0, 0.4) // RGB는 0~255 사이 정수
rgba(0.4, 0.31, 0, 0.4) // RGB가 0~1 사이 실수인 경우

이 premultiplied RGBA는 해석하자면 이런 뜻입니다.

R: 40% 강도의 붉은 빛을 내며, (100% 강도의 붉은 빛의 세기를 그 40% 만큼으로 줄여서)
G: 31% 강도의 초록 빛을 내며, (78% 강도의 초록 빛의 세기를 그 40% 만큼으로 줄여서)
B: 0% 강도의 푸른 빛을 낸다. (0% 강도의 푸른 빛의 세기를 그 40% 만큼으로 줄여서)
A: 덤으로 정보를 주자면, RGB 세 가지 각각의 빛의 세기를 그 40% 만큼으로 미리 줄여 놓았다. 미리 이 알파 값을 곱해 두었다.
