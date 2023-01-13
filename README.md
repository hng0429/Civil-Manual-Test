# Static Load Cases
## 기능
- 정적 단위하중조건을 정의하거나 이미 정의되어 있는 하중조건을 *수정* 또는 **삭제**합니다.
- 이 기능에서 입력된 정적 **단위하중 조건별**로 정적해석이 수행되며 각 해석결과는 ["Combinations"](http://manual.midasuser.com/KR/Civil/900/index.htm) 기능에서 상호조합될 수 있습니다. P-Delta 해석 또는 좌굴해석시 기하강성 행렬을 구성하는데 필요한 하중조합 조건을 부여하는데도 사용됩니다.
- Bridge Wizard 기능을 이용하여 교량 구조물의 시공단계 해석을 수행하는 경우는 하중의 성격을 고려하여 정적하중이 자동생성됩니다(Name 참조).
- midas Civil 을 사용하여 정적해석을 수행하는 절차는 다음과 같습니다.
    1. Load>Static Load Cases 메뉴로 단위하중 조건을 입력합니다.
    2. Load 메뉴의 각종 정적하중 입력기능을 이용하여 하중을 입력합니다.
    3. 하중재하모델에 기하비선형요소가 포함되어 있는 경우는 Load > ["Create Load Cases Using Combinations"](http://manual.midasuser.com/KR/Civil/900/index.htm)를 이용하여 미리 생성된 하중조합조건을 별도의 단위하중 조건으로 다시 지정한 후, Analysis>["Main Control Data"](http://manual.midasuser.com/KR/Civil/900/index.htm)메뉴를 이용하여 수렴에 필요한 반복수행회수와 수렴오차를 입력합니다.
    4. 해석과정에서 P-Delta 효과를 고려할 경우에는 Analysis>["P-Delta Analysis Control"](http://manual.midasuser.com/KR/Civil/900/index.htm)  메뉴를 이용하여 수렴에 필요한 반복수행회수와 수렴오차를 입력하고 기하강성행렬의 계산에 사용될 하중조건과 하중계수를 입력합니다.
    5. Analysis>["Perform Analysis"](http://manual.midasuser.com/KR/Civil/900/index.htm) 메뉴나 ![](http://manual.midasuser.com/KR/Civil/900/Start/05_Load/Image/Perform_Analysis.JPG) ["Perform Analysis"](http://manual.midasuser.com/KR/Civil/900/index.htm)를 클릭하여 해석을 수행합니다.
    6. 해석 진행과정 또는 해석 종료를 알리는 message가 화면 하단의 message window에 출력됩니다.
    7. 해석이 성공적으로 완료되면 하중조건이나 하중조합 조건을 이용하여 Results 메뉴의 각종 후처리 기능으로 해석결과를 분석합니다.
![](http://manual.midasuser.com/KR/Civil/900/Start/Common_image/IMG_C_ICON_NOTE_01.png)
<span style = "color: #0000FF"> 해석과정에서 나타나는 각종 message는 'fn.out'파일에 자동수록된다. </spna>

## 호출
- 메인 메뉴에서 [Load]탭>[Static Loads(Type)] 그룹 > [Static Load Cases]

## 입력
![](http://manual.midasuser.com/KR/Civil/900/Start/05_Load/Image/static_load_case.jpg)
*Static Load Cases 대화상자*

|<br><span style = "color: #0000FF">Case 1</span></br>  정적 단위하중 조건을 신규 정의하거나 추가 할 경우|다음 사항을 입력하고 ![](http://manual.midasuser.com/KR/Civil/900/Start/05_Load/Image/add_%EB%B2%84%ED%8A%BC.jpg)버튼을 클릭 합니다.   <br>**Name** : 정적 단위하중조건 이름</br>  ![](http://manual.midasuser.com/KR/Civil/900/Start/Common_image/IMG_C_ICON_NOTE_01.png)Bridge Wizard를 이용하여 교량 구조물의 시공단계 해석을 수행한 경우 시공단계 해석에 적용된 하중의 성격에 따라 다음과 같은 단위하중조건을 자동생성 합니다. 각 단위하중의 Load Type은 Construction Stage Load로 자동설정 됩니다. <br>**Self Weight** : 시공단계 해석에 적용된 요소의 자중</br>**Prestress** : 텐던에 도입된 프리스트레스<br>FT : FCM Wizard를 사용한 경우 이동식 거푸집(Form Traveler)의 자중</br> **Wet concrete** : FCM 또는 MSS/FSM Wizard를 사용한 경우 타설된 콘크리트(Wet concrete)의 자중  위의 하중조건은 전처리 모드에서 입력된 하중의 확인 등에 사용되고 해석시에는 시공단계 하중(Construction Load)로 통합된다. 해석결과의 확인은 시공단계 해석결과에 자동부여되는 별도의 하중조건에 대해 수행 할 수 있다. 자세한 설명은  ["Combinations"](http://manual.midasuser.com/KR/Civil/900/index.htm) 참조 <br>**Type** : 정적 단위하중종류 목록판에서 하중종류 선택</br> **Description** : 하중조건에 대한 간단한 설명문 입력|
|:---|:---|
|<br><span style = "color: #0000FF">Case 2</span></br>이미 정의된 하중조건을 수정 할 경우|대화상자 하부의 하중조건 목록표에서 해당조건을 선택하고 입력사항을 수정한 후, ![](http://manual.midasuser.com/KR/Civil/900/Start/05_Load/Image/modify_%EB%B2%84%ED%8A%BC.jpg)버튼을 클릭합니다.|
|<br><span style = "color: #0000FF">Case 3</span></br>이미 정의된 하중조건을 삭제 할 경우|<br>대화상자 하부의 하중조건 목록표에서 해당 하중조건을 선택하고, ![](http://manual.midasuser.com/KR/Civil/900/Start/05_Load/Image/delete_%EB%B2%84%ED%8A%BC.jpg)버튼을 클릭합니다.</br>![](http://manual.midasuser.com/KR/Civil/900/Start/Common_image/IMG_C_ICON_NOTE_01.png)<br><span style = "color: #0000FF"> 단위하중조건의 종류는 다음과 같다. 참고로 아래의 단위하중 조건 명칭은 각 규준에 명기된 것과 다를 수 있다.</span></br> ![](http://manual.midasuser.com/KR/Civil/900/Start/Common_image/IMG_C_ICON_DROP_DOWN.png) <details><br>User Define Load(U) : 사용자 정의하중</br>Dead Load(D) : 고정하중<br>Dead Load of Component and Attachments (DC)</br>Dead Load of Wearing Surfaces and Utilities (DW)<br>Downdrag (DD)</br>Earth Pressure (EP) : 토압<br>Horizontal Earth Pressure (EH) : 수평토압</br>Vertical Earth Pressure (EV) : 수직토압<br>Earth Surcharge Load (ES)</br>Locked in Erection Stresses (EL)<br>Live Load Surcharge (LS)</br></details>|
|왼쪽정렬|오른쪽정렬|
