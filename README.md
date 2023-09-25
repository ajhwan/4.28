# 1. 초음파센서와 객체인식을 통한 몰컴 프로젝트
<div>
    <img src="picture1.jpg" width="270" height="300">
    
    - 바탕화면 보이게 하는 버전(기본 모드)
</div>
    <img src="picture2.jpg" width="270" height="300">

    - ALT+TAB 버전(한 개의 LED 점등)
</div>    
    <img src="picture3.jpg" width="270" height="300">

    - 강제 종료 시키는 버전(두 개의 LED 점등)

# 2. 개발기간
2023.04.24 ~ 2023.04.26

# 3. 참여인원
1명

# 4. 개발환경
+ Arduino IDE 2.1 라이브러리 버전
+ VScode Python, openCV

# 5. 주요기능
+ 컴퓨터 모니터를 제어하는 3가지 모드가 있고 버튼을 눌러서 모드를 변경할 수 있다.
  + 초기상태 : 모니터 화면이 바탕화면을 보이게 하는 기능을 한다.
  + 버튼을 한 번 눌렀을 시 : ALT+TAP 기능을 한다.
  + 버튼을 두 번 눌렀을 시 : 컴퓨터를 종료 시키는 기능을 한다.
# 6. 주요코드
+ 키보드 제어를 위한 헤더파일

  ![head](https://user-images.githubusercontent.com/129160008/235062861-cd5156ca-600a-4bad-b7bb-cd09b83bcbec.PNG)


+ 모드를 바꾸기 위한 버튼 기능
    + 버튼을 누를 때마다 바뀌게 하려고 했지만 버튼이 2번눌리는 현상이 생겨서 HIGH에서 LOW가 될 때 모드를 바꾸는 것으로 변경

  ![button](https://user-images.githubusercontent.com/129160008/235062987-a32069da-38d7-4b46-ad07-7432d68b2741.PNG)
  
  
+ 3가지 모드에 대한 기능
    + 초기모드 : 윈도우 키+'D'를 사용한 바탕화면 보이기
    + 1버튼모드 : Alt+Tab 기능
    + 2버튼모드 : 윈도우 키+'X'+'U'+'U'를 이용한 컴퓨터 종료
  
  ![function](https://user-images.githubusercontent.com/129160008/235062995-ae3e482e-3e19-4c2b-bd13-76b2a2537dd1.PNG)
  
  
+ 컴퓨터와 시리얼 통신을 하기 위한 코드
  
  ![serial1](https://user-images.githubusercontent.com/129160008/235063006-64ad67da-b166-4cbb-b21b-9830acf215a0.PNG)
  
  
+ 얼굴이 감지된 뒤 신호를 보내기 위한 코드  
  
  ![serial2](https://user-images.githubusercontent.com/129160008/235063023-db060f3f-3615-4f63-9a8d-98e9d7b79338.PNG)


# 7. 데모
https://user-images.githubusercontent.com/129160008/235036656-0ab524e7-230e-4101-aa29-8532c26580d8.mp4

- 1.기본 버전으로 바탕화면을 보이는 모드
- 2.버튼을 한 번 눌렀을 때 모드로 ALT+TAB 기능을 하는 모드
- 3.버튼을 두 번 눌렀을 때 모드로 컴퓨터를 종료시키는 모드

# 8. 알려진 이슈
https://user-images.githubusercontent.com/129160008/235045723-aee8d609-1c09-4a5d-b065-e160a56d4ba4.mp4
+ 카메라와 아두이노 사이의 통신 딜레이가 생겨서 반응이 느리다.
+ 센서에도 인식되고 카메라에 얼굴이 인식되면 카메라에 얼굴이 인식되는 동안 같은 행동을 반복한다.(카메라에 인식되지 않아야 동작 멈춤)
    + 따라서 두가지 모드 보다 컴퓨터가 꺼지는 모드를 사용하는 것이 가장 유용하다고 판단된다.
