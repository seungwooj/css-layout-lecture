### 2. Grid

#### 2.1 CSS Grid Basic Concepts

- Grid : flexbox로 Grid(표)를 만들기가 어려워서 Grid전용 컨셉이 등장한 것
-
- **"father" is the grid container**  
  → write **"display: grid"** to the ~~direct father of the elemets you want to apply positioning~~
- **grid-template-columns** : 원하는 column수, 너비를 설정  
  (e.g. grid-template-columns: 250px 250px 200px;)
- **grid-template-rows** : 원하는 row수, 높이를 설정  
  (e.g. grid-template-rows: 100px 50px 30px;)
- **column-gap, row-gap**: column/row간의 공백을 설정  
  (e.g. column-gap: 10px; / row-gap: 10px)  
  → gap 만으로 설정시 row/column간의 공백을 동일하게 설정 가능  
  <img src="./img/grid-01.png" width="500px">

#### 2.2 Grid Template Areas

- **grid-template-areas**: grid의 각 공간에 들어갈 내용을 정의함
  → **father에 grid-template-area** 선언, 정의내용 작성  
  <img src="./img/grid-02-grid-template-areas.png" width="800px">  
  → **child에 grid-area** 선언, 각각의 child와 grid-area를 매칭 **(class이름과는 상관없음!)**  
  <img src="./img/grid-02-grid-area.png" width="500px">  
  cf> 특정 grid를 비울 때 : grid-template-areas에 " ."으로 표시

  **important!> grid가 적용되지 않는 경우**  
  **1. grid-area의 영역이 전부 이어져 있지 않을 때** (ex> header가 둘로 쪼개져 있을 경우, grid 반영 안됨)
  **2. grid-area의 영역이 직사각형이 아닐 때** (ex> header가 ㄴ자, ㄱ자 등일 경우, grid 반영 안됨)

#### 2.3 Rows and Columns & Shortcuts

- grid-template-area의 배경에 있는 기초 이론 -> **row line number, column line number**를 활용, ~~area를 정할 수 있음~~ (5rows = 6 row lines)
- **grid-row/column-start** : the area starts at certain row/column line number
- **grid-row/column-end** : the area ends at certain row/column line number
  → 각각의 element에 대해서 grid-area를 지정해서 grid-template-areas와 같은 효과를 줄 수 있다.
  <img src="./img/grid-04.png" width="800px">

#### 2.4 Shortcuts

- **grid-row/column : start / end** : grid-row/column-start, grid-row/column-end를 합친 shortcut
- **grid-row/column : start / -1** : grid-row/column : start~end (-1, -2 : 끝, 끝에서 2번째..)
- **grid-row.column : start / span no.of.spaces** : grid-row/column가 start로부터 no. of spaces를 차지

#### 2.5 Line naming

- grid-template-columns에서 각각의 line의 이름을 지정할 수 있음 (ex> [first-line] 200px )  
  → line의 이름으로 위의 shortcut 사용이 가능 (ex> grid-column : first-line / fourth-line)

#### 2.6 Grid Template

-
